# ImageReducer — third-party components

The ImageReducer application is distributed under the ImageReducer Attribution License. Dependencies retain their respective licenses. The application is provided without warranty. Share the entire portable package, including this file, `licenses` and `dependency-sources`.

| Component | Version | License / source |
|---|---|---|
| CPython | 3.12.14 | PSF and included notices; https://www.python.org/ |
| Tcl / Tk | 8.6.12 | BSD-style terms; https://www.tcl.tk/ |
| Pillow and its bundled image libraries | 12.3.0 | MIT-CMU and bundled notices in `licenses/pillow/LICENSE`; https://github.com/python-pillow/Pillow |
| pi-heif | 1.4.0 | BSD-3-Clause wrapper; wheel contains LGPL components; https://github.com/bigcat88/pillow_heif |
| libheif | 1.23.0 | LGPL-3.0; https://github.com/strukturag/libheif/tree/v1.23.0 |
| libde265 | 1.1.1 | LGPL-3.0; https://github.com/strukturag/libde265/tree/v1.1.1 |
| tkinterdnd2 | 0.6.3 | MIT; https://github.com/Eliav2/tkinterdnd2 |
| tkdnd | bundled by tkinterdnd2 | BSD-style terms; https://github.com/petasis/tkdnd |
| GCC runtime | bundled by pi-heif | GPL with GCC Runtime Library Exception; see included terms |
| MinGW-w64 runtime | bundled by pi-heif | notices in `licenses/MinGW-w64-COPYING.txt` |
| OpenSSL | bundled with CPython | Apache-2.0; https://www.openssl.org/ |
| PyInstaller bootloader | 6.22.2 | GPL with bootloader exception; https://pyinstaller.org/ |

Pillow's complete license file also includes the notices for its JPEG, PNG, WebP, and other codec components. This software is based in part on the work of the Independent JPEG Group.

The HEIC decoder is dynamically linked in `_internal`; no x265 HEIC encoder is bundled. `dependency-sources` contains the pi-heif source package with its build scripts and the libheif and libde265 source archives matching the versions reported by the bundled libraries. Full LGPLv3 and GPLv3 texts are in `licenses`. The upstream pi-heif bundled notice lists older library versions; the table above records the versions measured in this build.

Users may modify and replace the LGPL libraries and debug those modifications; ImageReducer imposes no prohibition on reverse engineering for that purpose. To rebuild the wrapper, extract `pi_heif-1.4.0.tar.gz` and follow its setup/build instructions with a compatible 64-bit toolchain. The library source archives include their CMake/build instructions. Preserve binary architecture and exported interfaces when replacing DLLs, or rebuild the wrapper and application against the modified libraries. Application source is not distributed. The LGPL decoder DLLs remain separately replaceable, and their corresponding source and wrapper build scripts are included in `dependency-sources`.

Microsoft Windows runtime DLLs accompany the Python runtime. They retain Microsoft's applicable redistribution terms; they are not covered by ImageReducer's application license.
