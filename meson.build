project('libxramdac', 'c',
        version: '0.1.0',
        meson_version: '>= 0.40.0',
        default_options: ['warning_level=1',
                          'buildtype=debugoptimized'])

libcvt_version = meson.project_version().split('.')

cc = meson.get_compiler('c')
mdep = cc.find_library('m', required : false)

prefix  = get_option('prefix')
inc = include_directories('include/libxramdac')

subdir('include')
subdir('lib')

pkg_mod = import('pkgconfig')
pkg_mod.generate(libraries : libxramdac,
                 version : '1.0',
                 name : 'libxramdac',
                 description : 'A Library to interface with external RAMDACs.')
