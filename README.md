# Ansible Role: Pip (for Python)

An Ansible Role that installs [Pip](https://pip.pypa.io) on Linux.

## Requirements

None.

## Role Variables
pip_package: python3-pip
pip_executable: pip3
A list of packages to install with pip. Examples below:

    pip_install_packages:
      # Specify names and versions.
      - name: docker
        version: "1.2.3"
      - name: awscli
        version: "1.11.91"
    
      # Or specify bare packages to get the latest release.
      - docker
      - awscli
    
      # Or uninstall a package.
      - name: docker
        state: absent
    
      # Or update a package to the latest version.
      - name: docker
        state: latest
    
      # Or force a reinstall.
      - name: docker
        state: forcereinstall
    
      # Or install a package in a particular virtualenv.
      - name: docker
        virtualenv: /my_app/venv

## Dependencies

None.

