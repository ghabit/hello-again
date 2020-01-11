    # project name and programming language
    project ('com.github.ghabit.hello-again', 'vala, 'c')

    # Create a new executable, list the files we want to compile, list the dependencies we nedd, and install executable(
        meson.project_name(),
        'src/Application.vala',
        dependencies: [
            depencency ('gtk+-3.0')
        ],
        install: true
    )

    # Install our .destop file so the Application Menu will see it
    install_data(
        join_paths('data', meson.project_name() + '.desktop'),
        install_dir: join_paths(get_option('datadir'), 'applications')
    )
    
    #Install our .appdata.xml file so AppCenter will see it 
    install_data(
        join_paths('data', meson.project_name() + '.appdata.xml'),
        install_dir: join_paths(get_option('datadir'), 'metainfo')
    )
