### Mutt configuraion with GnuPG-encrypted credentials, [solarized-dark](https://github.com/altercation/mutt-colors-solarized) colorscheme and vim-like keybindings



~/.mutt/credentials:
```
# imap
set imap_pass='verystrongpassword'
set imap_user='crash@example.org'
set folder='imaps://mail.example.org/'
set spoolfile='imaps://mail.example.org:993/'

# smtp
set smtp_url='smtp://crash@mail.example.org@mail.example.org:465/'
set smtp_pass='verystrongpassword'
```

Create gpg-encrypted credentials:

`gpg -r crash@example.org -e ~/.mutt/credentials`

Now, mutt will prompt for the gpg password after startup.

---

Terminal color fix: 

`export TERM=xterm-256color`
