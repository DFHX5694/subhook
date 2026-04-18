test_lib_sources = ['test_lib.c']
if host_machine.system() == 'windows'
  test_lib_sources += 'test_lib.def'
endif

test_lib = shared_library('test_lib',
  test_lib_sources,
  dependencies: subhook_dep,
)

test_prog = executable('test_prog',
  'test_prog.c',
  link_with: [test_lib, subhook_lib],
  include_directories: include_directories('..'),
)

test('test', test_prog)