project('miniasm', 'c',
  version : 'r55',
  license : 'MIT',
)

threads_dep = dependency('threads')
zlib_dep = dependency('zlib')

cc = meson.get_compiler('c')
libm = cc.find_library('m')

srcs = files([
  'asg.c',
  'asm.c',
  'common.c',
  'hit.c',
  'paf.c',
  'sdict.c',
  'sys.c'
])

includes = include_directories('.')

lib_miniasm = static_library('miniasm', [srcs])

miniasm_dep = declare_dependency(
  include_directories : [includes],
  dependencies : [libm, zlib_dep, threads_dep],
  link_with : [lib_miniasm],
)
