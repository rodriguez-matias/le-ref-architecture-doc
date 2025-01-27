# Workflow

!!! info "Leverage CLI"
    - We rely on the [**`leverage cli`**](../leverage-cli/install-leverage-cli.md) as a wrapper to run ansible commands
    that consistently use the same config files and secrets.
    
    - You are encouraged to read more about our [**`leverage cli`** how it works](../../how-it-works/leverage-cli/index.md) 
    section to better understand it.

!!! example "![leverage-ansible](../../assets/images/logos/ansible.png "Leverage"){: style="width:20px"} [Ansible Infra](https://github.com/binbashar/le-ansible-infra)"
    1. Get into the folder that you need to work with (e.g. `ansible-playbook-vpn-pritunl`)
    2. Run `leverage run init` to get all the necessary Ansible roles based on each `requirements.yml`
    4. Make whatever changes you need to make as stated in each Playbook Documentation (check Documentation section above)
    5. For a dry run execution use `leverage run apply\[--check\]` if you only mean to preview those changes
    6. Run `leverage run apply` if you want to apply those changes
    7. Run `leverage run apply\["--tags","common"\]` if you want to target specific playbook tasks by tag (eg: common tag) 