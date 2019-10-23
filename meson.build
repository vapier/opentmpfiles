project('opentmpfiles', ['c', 'cpp'],
  version : '0.1',
  default_options : ['warning_level=3'])


## Build libtmpfiles ##
libtmpfiles_src = [
  'src/set.c'
]

tmpfileslib = library('tmpfiles',
                      libtmpfiles_src,
                      version : meson.project_version(),
                      install : true)

libtmpfiles_dep = declare_dependency(
  link_with : tmpfileslib
)

## Build opentmpfiles ##
src = [
  'src/cli.c',
  'src/main.c',
]

executable('opentmpfiles',
           src,
           dependencies : libtmpfiles_dep,
           install : true)

subdir('test')
