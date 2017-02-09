# README.md
# Ansible Role: manage-users 1.0

This role is able to add/del users/groups, using booleans to activate/deactivate functions.

## Requirements

This role requires Ansible 2.2 or higher, and platform requirements are listed in the metadata file.

## Role Variables

Available variables are listed below, along with default values:

## Activate/deactivate functions
	loadlist: false
	addgroup: false
	adduser: false
	nonexpiring: false
	delgroup: false
	deluser: false
	showlists: false

### Users Parameters - Add users
	password: "{{item.key }}"	 	|| "{{ item.value.pwd }}"
	shell: 	  "{{ item.value.shell }}"	
	chg_pwd:  "Force-chg-pwd"		|| "Force-chg-pwd-Non-expiring" || "Do-not-chg-pwd-Non-expiring"
	update_pwd: "on_create" 		|| "always"
	non_unique: no				|| yes
	createhome: yes				|| no

## Dependencies
There is no dependencies with other roles.

## Modules
Added module "chage", created by @lqueryvg.

## Examples Playbook
1. Add groups from a list in a file, and users from a list in the playbook file. 
2. Delete users from a list in a file, and groups from a list in the playbook file. 

## License
GPLv3
