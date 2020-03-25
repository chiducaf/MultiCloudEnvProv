Role Name
=========

Installs Jenkins on RDebian/Ubuntu servers.

Requirements
------------

Requires curl to be installed on the server. Also, newer versions of Jenkins require Java 8.
Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

jenkins_package_state: present
The state of the jenkins package install. By default this role installs Jenkins but will not upgrade Jenkins (when using package-based installs). If you want to always update to the latest version, change this to latest.

jenkins_hostname: localhost
The system hostname; usually localhost works fine. This will be used during setup to communicate with the running Jenkins instance via HTTP requests.

jenkins_home: /var/lib/jenkins
The Jenkins home directory which, amongst others, is being used for storing artifacts, workspaces and plugins. This variable allows you to override the default /var/lib/jenkins location.

jenkins_http_port: 8080
The HTTP port for Jenkins' web interface.

jenkins_admin_username: admin
jenkins_admin_password: admin
Dependencies
-------
We need java installation.
Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: jenkins_test.yml }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
