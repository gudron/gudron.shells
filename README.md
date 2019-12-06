gudron.shells
=========

Roles for install operation system shell's

Role Variables
--------------

### General variables
  * `to_install: list`
    List of shell's where the environment will be prepared.

    Currently supported: `zsh`, `ash/dash`

    Full example: [defaults/main.yml](defaults/main.yml).

Example Playbook
----------------

    - hosts: example_project:&example_project_stage
      any_errors_fatal: "{{ any_errors_fatal | default(true) }}"
      gather_facts: True

      roles:
        - name: gudron.shells
          vars: 
            to_install:
              - zsh
              - ash

License
-------

Apache