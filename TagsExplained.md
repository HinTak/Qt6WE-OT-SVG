The number of tags is 8 higher than the number of releases. These early ones failed:

```
Qt6WE-OT-SVG-0.0
Qt6WE-OT-SVG-0.1
Qt6WE-OT-SVG-0.2
Qt6WE-OT-SVG-0.3
Qt6WE-OT-SVG-0.4
Qt6WE-OT-SVG-0.5
Qt6WE-OT-SVG-0.6
```

Annotation tag: `Qt6WE-OT-SVG-0.26-6.9.0-b3-13`

Tags `Qt6WE-OT-SVG-*-6.9.3-*` after `0.31` removed as "Ubuntu 24.04" getting filled with not enough disk space
and not usable.

`Qt6WE-OT-SVG-0.32-6.10.2-0` timed out:
```
2026-07-18T02:41:50.3744789Z pushd ~/rpmbuild/SPECS && rpmbuild -bb --noclean qt6-qtwebengine.spec && popd
...
2026-07-18T08:38:02.3431994Z [1307/2695] /usr/sbin/g++ ...
2026-07-18T08:38:04.4031626Z context canceled
2026-07-18T08:38:04.4180818Z ##[error]The operation was canceled.

2026-07-18T15:12:48.1414966Z pushd ~/rpmbuild/SPECS && rpmbuild -bb --noclean qt6-qtwebengine.spec && popd
...
2026-07-18T21:11:03.5094297Z [1412/2695] /usr/sbin/g++ ...
2026-07-18T21:11:17.0855334Z context canceled
2026-07-18T21:11:17.1022295Z ##[error]The operation was canceled.
```

`Qt6WE-OT-SVG-0.33-6.10.3-0` very close to 6 hours:

```
2026-07-19T00:55:40.3695819Z pushd ~/rpmbuild/SPECS && rpmbuild -bb --noclean qt6-qtwebengine.spec && popd
...
2026-07-19T06:53:32.0718831Z gdb-add-index: No index was created for /github/home/rpmbuild/BUILD/qt6-qtwebengine-6.10.3-build/BUILDROOT/usr/lib64/qt6/libexec/gn
2026-07-19T06:53:32.0720296Z gdb-add-index: [Was there no debuginfo? Was there already an index?]
2026-07-19T06:53:32.1311916Z readelf: Error: Unable to find program interpreter name
2026-07-19T06:54:36.8726628Z context canceled

2026-07-19T16:21:39.0165589Z pushd ~/rpmbuild/SPECS && rpmbuild -bb --noclean qt6-qtwebengine.spec && popd
...
2026-07-19T22:18:43.4736318Z Wrote: /github/home/rpmbuild/RPMS/x86_64/qt6-qtwebengine-debugsource-6.10.3-1i.fc42.x86_64.rpm
2026-07-19T22:20:29.1485777Z context canceled
```
