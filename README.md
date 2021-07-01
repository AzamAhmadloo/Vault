Role Name
=========

This role will install vault and give you a token for root login.


Role Variables
--------------

All variables are in defaults/main.yml


Example Playbook
----------------

Your playbook file could be same as bellow (Vault is this github repo folder name):

    ---
    - hosts: all
      become: yes
      become_user: root
      become_method: sudo
      vars:
        unseal_keys_dir_output: "{{ playbook_dir }}/unsealKey"
        root_token_dir_output: "{{ playbook_dir }}/rootKey"
      roles:
        - Vault

unseal_keys_dir_output: Playbook will create a directory named "unsealKey" and use it for saving the vault keys.
root_token_dir_output: Playbook will create a directory named "rootKey" and use it for saving the vault root token. 

Also you can remove variables.


Author Information
------------------

Customized and renewed by Azam ahmadloo (a.ahmadloo2013@gmail.com)
Base idea: https://github.com/MiteshSharma/AnsibleVaultRole
