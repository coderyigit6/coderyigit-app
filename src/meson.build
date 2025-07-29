pkgdatadir = get_option('prefix') / get_option('datadir') / meson.project_name()
moduledir = pkgdatadir / 'coderyigit_app'

python = import('python')

conf = configuration_data()
conf.set('PYTHON', python.find_installation('python3').full_path())
conf.set('pkgdatadir', pkgdatadir)
configure_file(
            input: 'coderyigit-app.in',
           output: 'coderyigit-app',
    configuration: conf,
          install: true,
      install_dir: get_option('bindir'),
     install_mode: 'r-xr-xr-x'
)

coderyigit_app_sources = [
    '__init__.py',
    'main.py'
]

install_data(coderyigit_app_sources, install_dir: moduledir)
