    # project name and programming language
    project ('com.github.ghabit.hello-again', 'vala', 'c')
    
    # Include the translations module
    i18n = import('i18n')
    
    # Setour translation domain
    add_global_arguments(-DGETTEXT_Package="@0@"'.fomrat (meson.project_name()), language:'c')
    
    # Create a new executable, list the files we want to compile, list the dependencies we nedd, and install
    executable(
        meson.project_name(),
        'src/Application.vala',
        dependencies: [
            dependency ('gtk+-3.0')
        ],
        install: true
    )

    #Translate and install our .desktop file
    i18n.merge_file(
        input: join_paths('data', meson.project_name() + '.desktop.in'),
        output: meson.project_name() + '.desktop',
        po_dir: join_paths(meson.source_root(), 'po').
        type: 'desktop',
        install: true,
        install_dir: join_paths(get_option('datadir'), 'applications')
    )
    
    #Translate and install our .appdata file
    i18n.merge_file(
        input: join_paths('data', meson.project_name() + '.appdate.xml.in'),
        output: meson.project_name() + '.appdata.xml',
        po_dir: join_paths(meson.source_root(), 'po'),
        install: true,
        install_dir: join_paths(get_option('datadir'), 'metainfo')
    )
