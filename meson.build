project('minissd', 'c',
  default_options: ['c_std=c99'])

inc = include_directories('include')

minissd = static_library(
  meson.project_name(),
  'src/minissd.c',
  'include/minissd.h',
  include_directories: inc,
)

minissd_dep = declare_dependency(
  include_directories: inc,
  link_with: minissd)

meson.override_dependency('minissd', minissd_dep)

if get_option('examples')
    executable(
      'minissd_example_print',
      'example/minissd_print.c',
      dependencies: minissd_dep)
endif

if get_option('tests')
  subdir('tests')
endif
