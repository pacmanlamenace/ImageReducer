# ImageReducer 1.3.0

Free bulk image compression for Windows. Works entirely on your computer—no account, uploads, or subscription.

## Start

Extract the entire portable ZIP to a folder, then double-click **ImageReducer.exe**. Keep the `_internal` folder beside the executable. Python and Microsoft HEIC extensions are not required. Built for 64-bit Windows 10/11; other platforms are not supported by this package.

## Compress images

1. Drag images or folders onto the window, or use **Add images** / **Add folder**. Folder selection includes the immediate files, not nested folders.
2. Choose **1 MB**, **2 MB**, or **Custom** under Maximum per image. For a custom limit, enter a number and choose MB or KB. Decimals work: `1.5` MB, for example. Limits range from 10 KB to 1,000 MB. One MB means 1,000,000 bytes.
3. Choose an export format. **Auto** uses JPEG for opaque images and WebP for images with transparency. JPEG, WebP, and PNG can also be selected explicitly.
4. Choose your **Save folder** with Browse, or type a path. ImageReducer remembers it for the next launch; new folders are created when the batch starts.
5. Click **Compress images**. Every successfully saved file is strictly below your chosen limit. The app first adjusts compression, then reduces pixel dimensions while keeping proportions.
6. Use **Open save folder** to see results or **Export report** to save a CSV with output paths, sizes, dimensions, and errors.

## Your originals

Original files are never edited or deleted. Set the **Prefix** and **Suffix** fields to choose output names; a live example appears underneath. For example, prefix `small_` and suffix `_share` turn `holiday.jpg` into `small_holiday_share.jpg`. Either field can be blank; both are remembered for next time. The initial suffix is `_fit`. Each field accepts up to 60 characters; Windows-invalid filename characters are rejected before the batch begins.

If a name is already taken, the app adds a number. This also protects originals when both naming fields are blank and the save folder is the source folder. Running a batch again creates another set of copies.

## Compact window

The default window is smaller than the previous release. Compression, cancellation, output-folder, and report buttons stay in a fixed bottom area. The middle section scrolls vertically (or horizontally at very narrow widths) so settings remain accessible on small screens or with larger Windows text. Use the scrollbars or mouse wheel outside the file list. The file list has its own scrollbar.

On first launch, ImageReducer imports the previous PhotoFit Free save-folder setting if available. It then saves settings separately under the new name.

## Supported images

Input: JPG, JPEG, WebP, HEIC/HEIF, PNG, BMP.

Output: JPEG, WebP, PNG. HEIC and BMP inputs are converted to the selected output format. These formats are better suited to small, shareable files. JPEG output gives transparent areas a white background; Auto, WebP, and PNG preserve transparency. PNG is lossless at each output resolution, but may need substantial resizing to meet a small limit.

Only the first frame or primary image is exported from animated images or multi-image files. Output is 8-bit; HDR/high-bit-depth information is not retained. Camera orientation is applied to the pixels. Camera/GPS metadata is removed from copies; embedded color profiles are retained. Very large, corrupt, or unsupported images may fail individually; the rest of the batch continues. An image whose minimum encoding and color profile cannot fit the limit is reported as a failure.

Images already below the limit are still exported in the selected format and may be recompressed. The selected value is an upper bound, not a target the app tries to fill exactly.

## Cancel and troubleshoot

Cancel stops at the next safe point in image processing. Finished files remain available. Wait for cancellation to finish before closing the window. Large images may take longer, and the app processes one image at a time to keep memory use reasonable.

For save errors, choose a writable folder and check available disk space. For decode errors, try opening the original in another image viewer. The full error text is available in the exported CSV. For a missing `_internal` error, extract the entire ZIP again instead of moving only the EXE.

This build is unsigned. Windows may display an unknown-publisher warning; no certificate or installer is included.

## Settings and uninstall

The default folder is stored in `%APPDATA%\ImageReducer\settings.json`. To uninstall, delete the extracted application folder. Optionally delete that settings folder. Your original and exported images are unaffected.

## Distribution and credit

ImageReducer by **CTP · ctp@ctp.cc**. Click the bottom-right credit to read the license in the app.

You may use and redistribute the application under the included ImageReducer Attribution License. Redistributed copies must retain visible CTP credit in the interface, accompanying documentation, and the redistributor's download page. Read `LICENSE.txt` for the full conditions.

Application source is not included. Required third-party license notices and decoder source materials are included separately; those components retain their own terms.
