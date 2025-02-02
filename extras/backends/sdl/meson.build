ma_backend_sdl_srcs = files(
  'backend_sdl.c',
  'backend_sdl.h',
)
if ma_impl_workaround
  ma_extra_srcs += ma_backend_sdl_srcs
else
  # linking to sdl is handled in top-level
  ma_all_libs += static_library(
    'ma_backend_sdl',
    ma_backend_sdl_srcs,
    dependencies: ma_sys_deps + sdl_dep,
    install: false,
    pic: true,
  )
endif
