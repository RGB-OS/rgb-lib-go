run for darwin
#cgo darwin LDFLAGS: -lrgblibuniffi -L${SRCDIR}/lib -Wl,-rpath,${SRCDIR}/lib
install_name_tool -id @rpath/librgblibuniffi.dylib lib/librgblibuniffi.dylib

