Role Name
=========

Installs Java for Debian/Ubuntu linux servers.

Requirements
------------

None.
Role Variables
--------------
vailable variables are listed below, along with default values:

# The defaults provided by this role are specific to each distribution.
java_packages:
  - java-1.8.0-openjdk
Set the version/development kit of Java to install, along with any other necessary Java packages. Some other options include are included in the distribution-specific files in this role's 'defaults' folder.

java_home: ""
If set, the role will set the global environment variable JAVA_HOME to this value.

Dependencies
------------

None.
Example Playbook
----------------

    - hosts: server
      roles:
         - { role: java_test.ym }

