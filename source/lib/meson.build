lib_sources = files (
    'ShaderBin.vala',
    'ShaderPaintable.vala',
    'ShaderStack.vala',
    'ShaderToy.vala',
)

lib_inc = include_directories ('.')

lib_dependencies = [
    dependency ('gtk4', version: '>=4.0.0'),
    dependency ('glib-2.0'),
    dependency ('gobject-2.0'),
]

shader_lib = static_library (
    'shaderlibrary',
    sources: lib_sources,
    dependencies: lib_dependencies,
    install: true,
    install_dir: [true, true, true],
)

shader_dep = declare_dependency (
    include_directories: lib_inc,
    link_with: shader_lib,
)