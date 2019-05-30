project('uftpd', 'c',
   version : '2.7',
   default_options : ['c_std=gnu99'],
   )



src = ['src/uftpd.c',
       'src/tftpcmd.c',
       'src/log.c',
       'src/ftpcmd.c',
       'src/common.c']

lite = dependency('libite')
libuev = dependency('libuev')

conf_data = configuration_data()

conf_data.set('package', meson.project_name())
conf_data.set('version', meson.project_version())
conf_data.set('bugsurl', 'https://github.com/troglobit/uftpd/issues')
conf_data.ser('homepage', 'http://troglobit.com/uftpd.html')

configure_file(input : 'mesonconfig.h.in',
  output : 'config.h',
  configuration : conf_data)

configuration_in = include_directories('.')

executable('uftpd', src,
	   dependencies : [lite, libuev],
   	   c_args : ['-W', '-Wall', '-Wextra',
           	    '-Wno-unused-parameter',],
  	   cpp_args :['-D_GNU_SOURCE', '-D_BSD_SOURCE',
           	      '-D_DEFAULT_SOURCE'],
	   include_directories : configuration_in)
