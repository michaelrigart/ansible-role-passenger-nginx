Ansible Passenger-Nginx Role
============================

An ansible role for installing and configuring Passenger with Nginx.

Role Variables
--------------

passenger_nginx_apt_https: list of packages to install packages of https
passenger_nginx_apt_pkgs: list of packages to install passenger-nginx
passenger_nginx_pkg_version: specify the specific package version you wish to install
When specifying a version, the state will be forced to installed. When omitting the variable or leaving it empty
passenger_nginx_path: specify path where nginx configuration files are located
passenger_nginx_conf_path: specify nginx conf.d path
passenger_nginx_pkg_state: indicates the package state; Allowed setting: installed, latest
passenger_nginx_service_state: indicates the service state; Allowed setting: started, stopped
passenger_nginx_service_enabled: indicates if service needs to be enabled on boot; Allowed settings: yes, no
passenger_nginx_nginx_config: dictionary that holds the full nginx configuration
passenger_nginx_passenger_config: dictionary that holds the full passenger congiruation
passenger_nginx_custom_directories: list of dictionaries that hold custom directories that might be needed
passenger_nginx_logrotate_config: list of dictionaries for logrotate configurations

View the default vars - defaults/main.yml - for a more detailed example.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: MichaelRigart.passenger-nginx }

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>