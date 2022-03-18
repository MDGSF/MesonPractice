project('HelloSDL2', 
    'c',
    default_options: 'default_library=static'
)

sdl2_dep = dependency('sdl2')

executable('hello', 'main.c', 
	win_subsystem: 'windows',
    dependencies: sdl2_dep
)

