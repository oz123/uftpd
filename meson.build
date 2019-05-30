project('uftpd', 'c',
   version : '2.7.0',
   default_options : ['c_std=gnu99'],
   c_args : ['-W', '-Wall', '-Wextra',
             '-Wno-unused-parameter',],
   cpp_args :['-D_GNU_SOURCE', '-D_BSD_SOURCE',
             '-D_DEFAULT_SOURCE']
   )


src = ['src/uftpd.c',
       'src/tftpcmd.c',
       'src/log.c',
       'src/ftpcmd.c',
       'src/common.c']

lite = dependency('libite')
libuev = dependency('libuev')

executable('uftpd', src,
	   dependencies : [lite, libuev],
	   )
