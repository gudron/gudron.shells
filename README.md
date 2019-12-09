gudron.shells
=============

Ansible role for install operation system shell's

Role Variables
--------------

### General variables
  * `to_install: list`
    List of shell's where the environment will be prepared.

    Currently supported: `zsh`, `ash/dash`

    Full example: [defaults/main.yml](defaults/main.yml).

Instalation
-----------

Add **gudron.sudo** role to your *requirements* file.

```yaml
  - src: git@github.com:gudron/gudron.shells.git
    scm: git
    version: master
```

Install roles via **ansible-galaxy** tool.

```bash
ansible-galaxy install -p roles -r requirements.yml
```

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