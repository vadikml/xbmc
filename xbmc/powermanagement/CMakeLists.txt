set(SOURCES DPMSSupport.cpp
            IPowerSyscall.cpp
            PowerManager.cpp)

set(HEADERS DPMSSupport.h
            IPowerSyscall.h
            PowerManager.h)

core_add_library(powermanagement)
add_dependencies(powermanagement libcpluff)

if(ENABLE_INTERNAL_FFMPEG)
  add_dependencies(powermanagement ffmpeg)
endif()
