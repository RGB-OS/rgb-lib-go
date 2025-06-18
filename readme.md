run for darwin
#cgo darwin LDFLAGS: -lrgblibuniffi -L${SRCDIR}/lib -Wl,-rpath,${SRCDIR}/lib
install_name_tool -id @rpath/librgblibuniffi.dylib lib/librgblibuniffi.dylib
run for linux
patchelf --set-rpath '$ORIGIN/lib' lib/librgblibuniffi.so

publish
git tag v0.3.5  
git push origin v0.3.5