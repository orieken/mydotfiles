# mydotfiles

```
nvm is not compatible with the npm config "prefix" option: currently set to "/usr/local"
Run `npm config delete prefix` or `nvm use --delete-prefix vX.X.X --silent` to unset it.
```
### Cause
left over files from system node install

### Fix

```
➜ brew uninstall nvm \n
➜ brew prune
➜ rm -rf /usr/local/{lib/node{,/.npm,_modules},bin,share/man}/{npm*,node*,man1/node*}
➜ brew install nvm
➜ nvm install X
```
