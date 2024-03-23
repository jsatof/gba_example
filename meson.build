project('gba_example', 'c',
  default_options : ['c_std=c99'])

build_cc = meson.get_compiler('c', native : true) # x86_64
host_cc = meson.get_compiler('c', native : false) # arm

m_dep_build = build_cc.find_library('m', required : false)
m_dep_host = host_cc.find_library('m', required : false)

native_exec = executable('gba_example',
  'src/main.c',
  dependencies : [m_dep_build])

host_exec = executable('gba_example_arm',
  'src/main.c',
  dependencies : [m_dep_host])
