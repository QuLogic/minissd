add_languages('cpp')

gtest = dependency('gtest', main: true, fallback: ['gtest', 'gtest_main_dep'])

minissd_tests = executable(
  'minissd_tests',
  'src/test_parser.cpp',
  dependencies: [minissd_dep, gtest],
)

test('minissd', minissd_tests, protocol: 'gtest')
