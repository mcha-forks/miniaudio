ma_backend_pipewire_srcs = files(
  'miniaudio_pipewire.c',
  'miniaudio_pipewire.h',
)
if ma_impl_workaround
  ma_extra_srcs += ma_backend_pipewire_srcs
else
  # linking to pipewire is handled in top-level
  ma_all_libs += static_library(
    'ma_backend_pipewire',
    ma_backend_pipewire_srcs,
    dependencies: ma_sys_deps + pipewire_dep,
    install: false,
    pic: true,
  )
endif
