project('subhook', 'c',
  version: '0.2.1',
  default_options: ['warning_level=1']
)

add_project_arguments('-DSUBHOOK_STATIC', language: 'c')

subhook_headers = files('subhook.h')
subhook_sources = files('subhook.c', 'subhook_private.h')

subhook_lib = static_library('subhook',
  subhook_sources,
  install: true,
  install_dir: 'lib',
  pic: false
)

subhook_dep = declare_dependency(
  sources: subhook_sources,
  include_directories: include_directories('.')
)

install_data('subhook.h', install_dir: 'include')
