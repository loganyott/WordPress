# loganyott/wordpress

## Local Environment Setup

1. `vagrant up`

### Note:
If you don't want to type your password on every `vagrant up` for nfs mounting, add this to your `/etc/sudoers` file.
```bash
Cmnd_Alias VAGRANT_EXPORTS_ADD = /usr/bin/tee -a /etc/exports
Cmnd_Alias VAGRANT_NFSD = /sbin/nfsd restart
Cmnd_Alias VAGRANT_EXPORTS_REMOVE = /usr/bin/sed -E -e /*/ d -ibak /etc/exports
%admin ALL=(root) NOPASSWD: VAGRANT_EXPORTS_ADD, VAGRANT_NFSD, VAGRANT_EXPORTS_REMOVE
```

## Tips and Tricks

WP-CLI is installed by default. You can access it after a `vagrant ssh` via the `wp` command.
