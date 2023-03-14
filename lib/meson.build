libxramdac_sources = [
    'xf86RamDac.c',
    'xf86RamDacCmap.c',
    'IBM.c',
    'BT.c',
    'TI.c',
]

add_global_arguments('-I/usr/X11/include/xorg', '-I/usr/X11R7/include/pixman-1', language : 'c')

libxramdac = shared_library('xramdac',
                         libxramdac_sources,
                         include_directories : inc,
                         install : true)
