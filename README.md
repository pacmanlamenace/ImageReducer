<p align="center"><img src="assets/ImageReducer-logo.png" alt="ImageReducer logo" width="140"></p>
<h1 align="center">ImageReducer</h1>
<p align="center">Free, offline bulk image compression for Windows.</p>
<p align="center"><strong>ImageReducer by CTP · <a href="mailto:ctp@ctp.cc">ctp@ctp.cc</a></strong></p>

## Download

**[Download ImageReducer for Windows x64](https://github.com/pacmanlamenace/ImageReducer/releases/latest)**

Extract the entire Windows ZIP and run **ImageReducer.exe**. Keep its `_internal` folder beside it. No separate Python installation is needed. Built for Windows 10/11, 64-bit. The portable executable is unsigned, so Windows may show an unknown-publisher warning.

## Features

- Bulk drag-and-drop or selection of JPG, JPEG, WebP, HEIC/HEIF, PNG, and BMP.
- A maximum per image: 1 MB, 2 MB, or a custom limit in MB or KB.
- Automatic compression and resizing; every successful output is strictly below the selected limit.
- Export as JPEG, WebP, or PNG. Auto selects JPEG for photos and WebP for transparency.
- Remembered save folder, editable filename prefix/suffix, and a live name preview.
- Originals are preserved; existing output files are never overwritten.
- Compact window with fixed compression buttons, cancellation, and CSV reports.
- Local processing, with no uploads, telemetry, account, or subscription.

## Quick start

1. Add images or drop a folder onto the app.
2. Choose the maximum file size and output format.
3. Set your optional prefix/suffix and save folder.
4. Click **Compress images**.

One MB is 1,000,000 bytes. Smaller limits can reduce quality and resolution. HEIC/BMP are converted to the selected export format. Only the first frame or primary image is exported from animated or multi-image input. See the [user guide](USER-GUIDE.md) for details.

## License and attribution

This release is free to use and redistribute under the **[ImageReducer Attribution License](LICENSE.txt)**. Redistributed or modified versions must retain the CTP credit visibly in their interface and in accompanying documentation and download pages. Click the credit in the app to read the license.

This repository contains downloads, branding, and documentation; **application source code is not distributed here**. Independently licensed third-party components retain their own terms. Required decoder source archives and third-party notices accompany the Windows release.


## Documentation

- [User guide](USER-GUIDE.md)
- [Release notes](RELEASE-NOTES.md)
- [Third-party notices](THIRD-PARTY-NOTICES.md)
- [Test results](TEST-RESULTS.json)

**CTP · [ctp@ctp.cc](mailto:ctp@ctp.cc)**

[Report an issue](https://github.com/pacmanlamenace/ImageReducer/issues). Include your Windows version and error message; avoid uploading private photos.
