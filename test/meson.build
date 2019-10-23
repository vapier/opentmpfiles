test_src = [
  'cli_test.cc',
  'set_test.cc',
  'xfuncs_test.cc'
]

inc = include_directories('../src')

gtest_dep = dependency('gtest', main : true, fallback : ['gtest', 'gtest_main_dep'])

e = executable('tmpfiles_test',
               test_src,
               include_directories : inc,
               dependencies : [gtest_dep, libtmpfiles_dep])
test('test', e)
