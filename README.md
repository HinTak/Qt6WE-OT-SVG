`rpm --rebuild ...` takes 5 hours 23 minutes:

```
2023-12-16T23:51:23
2023-12-17T05:14:09
```

From build log:

```
/github/home/rpmbuild/BUILD
/github/home/rpmbuild/SOURCES
src/3rdparty/chromium/
~/rpmbuild/BUILD/qtwebengine-everywhere-src-6.6.1
src/3rdparty/chromium/third_party/blink/renderer/
 [196/196] LINK gn
/github/home/rpmbuild/BUILD/qtwebengine-everywhere-src-6.6.1/redhat-linux-build/src/pdf/RelWithDebInfo/x86_64/args.gn
 -- GN Done. Made 17662 targets from 2873 files in 12189ms
/github/home/rpmbuild/BUILD/qtwebengine-everywhere-src-6.6.1/redhat-linux-build/src/core/RelWithDebInfo/x86_64/args.gn
 -- GN Done. Made 17604 targets from 2863 files in 12530ms
 [30094/30094] touch QtWebEngineCore.stamp
 Provides: bundled(angle) bundled(chromium) = 102.0.5005.177 bundled(skia)
 src/3rdparty/chromium/third_party/skia/modules/
 src/3rdparty/chromium/third_party/blink/renderer/
 ../../../../../src/3rdparty/chromium/third_party/skia/src/core/SkFontDescriptor.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/core/SkFontMgr.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/core/SkFontStream.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/core/SkFont.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/core/SkFont_serial.cpp
../../../../../src/3rdparty/chromium/pdf/font_table_linux.cc
../../../../../src/3rdparty/chromium/skia/ext/fontmgr_default.cc
../../../../../src/3rdparty/chromium/skia/ext/fontmgr_default_linux.cc
../../../../../src/3rdparty/chromium/third_party/skia/src/utils/SkOrderedFontMgr.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/utils/mac/SkCTFont.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/utils/win/SkDWriteFontFileStream.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/fonts/SkRemotableFontMgr.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/fonts/SkFontMgr_indirect.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontConfigInterface.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontHost_FreeType.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontConfigInterface_direct_factory.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontConfigInterface_direct.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontHost_FreeType_common.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontMgr_android_parser.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontMgr_FontConfigInterface.cpp
../../../../../src/3rdparty/chromium/third_party/skia/src/ports/SkFontMgr_android.cpp
../../../../../src/3rdparty/chromium/third_party/blink/renderer/platform/fonts/font_matching_metrics.cc
```