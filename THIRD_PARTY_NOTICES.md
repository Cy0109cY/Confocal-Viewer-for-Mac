# 第三方软件声明 / Third-Party Notices

**Confocal Viewer for Mac** 自身代码以 MIT 许可证发布（见 [LICENSE](LICENSE)）。软件在运行或分发时使用了下列第三方开源组件，它们各自保留自己的版权和许可证。完整许可证文本在 [`third_party_licenses/`](third_party_licenses/) 目录中，随应用一起分发（应用包内的 `third_party_licenses/` 文件夹）。

This application uses the open-source components listed below. Each keeps its own copyright and licence; full licence texts are in the `third_party_licenses/` folder shipped with the app.

## LGPL-3.0 组件（需要特别说明）

以下组件使用 **GNU LGPL v3**。你有权获得它们的源码，并可以用自己修改或编译的版本替换它们：

- **Qt for Python (PySide6 / Shiboken6) 与 Qt 库** — 源码获取：https://code.qt.io/cgit/pyside/pyside-setup.git/ ，Qt 源码：https://download.qt.io/official_releases/qt/
- **pylibCZIrw（静态包含 libCZI）** — 源码获取：https://github.com/ZEISS/pylibczirw ，libCZI：https://github.com/ZEISS/libczi

**如何替换：** 本应用以目录形式分发（不是单文件打包）。Qt / PySide6 库位于应用包内 `Contents/Frameworks/PySide6/`，pylibCZIrw 位于 `Contents/Frameworks/_pylibCZIrw.cpython-312-darwin.so` 与 `Contents/Frameworks/pylibCZIrw/`，都是独立文件，可以直接替换为兼容版本的同名文件。LGPL 全文见 [`third_party_licenses/LGPL-3.0.txt`](third_party_licenses/LGPL-3.0.txt)（它引用的 GPL 全文见 [`GPL-3.0.txt`](third_party_licenses/GPL-3.0.txt)）。

**Qt 模块范围：** 本应用只使用 Qt 的 QtCore、QtGui、QtWidgets、QtOpenGL、QtOpenGLWidgets 等基础模块。Qt for Python 的发行包默认带有更多 Qt 模块，打包脚本（`tools/postbuild.sh`）会在构建后移除其中未使用、且许可证条件不同的 **Qt Virtual Keyboard**，它不随本软件分发。其余随附的 Qt 模块在 LGPL-3.0 下使用。

PySide6 / Qt 同时提供 LGPL-3.0 / GPL-2.0 / GPL-3.0 / 商业许可，本软件按 **LGPL-3.0** 使用它们。

## 组件列表

| 组件 | 版本 | 许可证 | 主页 | 随附许可证文件 |
|:--|:--|:--|:--|:-:|
| annotated-types | 0.8.0 | MIT | <https://github.com/annotated-types/annotated-types> | 1 |
| cffi | 2.1.1 | MIT-0 | <https://cffi.readthedocs.io/> | 1 |
| cloudpickle | 3.1.2 | BSD-3-Clause | <https://github.com/cloudpipe/cloudpickle> | 1 |
| dask | 2026.8.0 | BSD-3-Clause | <https://github.com/dask/dask/> | 3 |
| fsspec | 2026.9.0 | BSD-3-Clause | <https://filesystem-spec.readthedocs.io/en/latest/> | 1 |
| imagecodecs | 2026.8.16 | BSD-3-Clause | <https://www.cgohlke.com> | 67 |
| liffile | 2026.7.14 | BSD-3-Clause | <https://www.cgohlke.com> | 1 |
| locket | 1.0.0 | BSD-2-Clause | <http://github.com/mwilliamson/locket.py> | 1 |
| nd2 | 0.12.0 | BSD 3-Clause License | <https://github.com/tlambert03/nd2> | 1 |
| numpy | 2.5.3 | BSD-3-Clause AND 0BSD AND MIT AND Zlib AND CC0-1.0 | <https://numpy.org> | 19 |
| ome-types | 0.6.3 | MIT | <https://github.com/tlambert03/ome-types> | 1 |
| packaging | 26.3 | Apache-2.0 OR BSD-2-Clause | <https://packaging.pypa.io/> | 3 |
| partd | 1.4.2 | BSD | <http://github.com/dask/partd/> | 1 |
| pillow | 12.3.0 | MIT-CMU | <https://pillow.readthedocs.io> | 1 |
| pycparser | 3.0 | BSD-3-Clause | <https://github.com/eliben/pycparser> | 1 |
| pydantic | 2.13.5 | MIT | <https://github.com/pydantic/pydantic> | 1 |
| pydantic-extra-types | 2.11.1 | MIT | <https://github.com/pydantic/pydantic-extra-types> | 1 |
| pydantic_core | 2.46.5 | MIT | <https://github.com/pydantic/pydantic> | 1 |
| pylibCZIrw | 6.1.0 | GNU Lesser General Public License v3 (LGPLv3) | <https://github.com/ZEISS/pylibczirw> | 3 |
| PyNaCl | 1.6.2 | Apache-2.0 | <https://github.com/pyca/pynacl/> | 2 |
| PyOpenGL | 3.1.10 | BSD License | <https://pyopengl.sourceforge.net/> | 3 |
| PySide6 | 6.11.2 | LGPL-3.0-only OR GPL-2.0-only OR GPL-3.0-only | <https://www.qt.io/qt-for-python> | — |
| PySide6_Addons | 6.11.2 | LGPL-3.0-only OR GPL-2.0-only OR GPL-3.0-only | <https://www.qt.io/qt-for-python> | — |
| PySide6_Essentials | 6.11.2 | LGPL-3.0-only OR GPL-2.0-only OR GPL-3.0-only | <https://www.qt.io/qt-for-python> | — |
| PyYAML | 6.0.3 | MIT | <https://pyyaml.org/> | 1 |
| resource-backed-dask-array | 0.1.0 | BSD-3-Clause | <https://github.com/tlambert03/resource-backed-dask-array> | 1 |
| scipy | 1.18.1 | BSD-3-Clause（另含若干组件，见随附文件） | <https://scipy.org/> | 2 |
| shiboken6 | 6.11.2 | LGPL-3.0-only OR GPL-2.0-only OR GPL-3.0-only | <https://www.qt.io/qt-for-python> | — |
| tifffile | 2026.9.20 | BSD-3-Clause | <https://www.cgohlke.com> | 1 |
| toolz | 1.1.0 | BSD-3-Clause | <https://github.com/pytoolz/toolz> | 1 |
| typing-inspection | 0.4.4 | MIT | <https://github.com/pydantic/typing-inspection> | 1 |
| typing_extensions | 4.16.0 | PSF-2.0 | <https://typing-extensions.readthedocs.io/> | 1 |
| validators | 0.35.0 | MIT | <https://python-validators.github.io/validators> | 1 |
| xmltodict | 1.0.4 | MIT | <https://github.com/martinblech/xmltodict> | 1 |
| xsdata | 26.2 | MIT | <https://github.com/tefra/xsdata> | 1 |
| Python | 3.12 | PSF-2.0 | <https://www.python.org/> | 见 `third_party_licenses/Python/` |
| Tcl/Tk（随 Python 一起打包） | 9.0 | Tcl/Tk License（类 BSD） | <https://www.tcl.tk/software/tcltk/license.html> | — |

## imagecodecs 自带的原生编解码库

`imagecodecs` 的预编译包内含下列第三方压缩 / 图像编解码库（位于应用包 `Contents/Frameworks/` 下的 `.dylib`），各自的许可证文件已收录在 `third_party_licenses/imagecodecs/`：

aom, bcdec, bitshuffle, blosc, blosc2, brotli, brunsli, bzip2, cfitsio, charls, dav1d, fastlz, giflib, hdf5, heif, highway, isa-l, jetraw, jpeg, jpg_0xc3, jxrlib, lcms2, lerc, libaec, libaivf, libdeflate, libjpeg, libjpeg-turbo, libjxl, libjxs, liblj92, liblzma, libmng, libpng, libspng, libtiff, libultrahdr, libwebp, libxml2, libyuv, lz4, lzf, lzfse, lzham, lzokay, meshoptimizer, mozjpeg, netcdf-c, openexr, openjpeg, openjph, openzl, pcodec, postgresql, qoi, rav1e, snappy, sperr, svt-av1, sz3, wavpack, zfp, zlib, zlib-ng, zopfli, zstd

## 说明

- 本清单由 `tools/gen_third_party_notices.py` 根据构建环境中安装的包自动生成；升级依赖后请重新运行。
- 许可证信息来自各包的元数据与随包文件，不构成法律意见。
- 本软件与 Carl Zeiss、Nikon、Leica 等公司无关；相关名称是其所属公司的商标，这里仅用于说明所支持的文件格式。
