include_directories(inc)

if(CLR_CMAKE_HOST_WIN32)
  add_subdirectory(corerun)
  add_subdirectory(coreconsole)
  add_subdirectory(coreshim)
else(CLR_CMAKE_HOST_WIN32)
  add_subdirectory(unixcoreruncommon)
  add_subdirectory(unixcorerun)
  add_subdirectory(unixcoreconsole)
  if(CLR_CMAKE_HOST_DARWIN)
    add_subdirectory(osxbundlerun)
  endif(CLR_CMAKE_HOST_DARWIN)
endif(CLR_CMAKE_HOST_WIN32)
