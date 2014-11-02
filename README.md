# plushu buildpack management commands

This plugin contains commands for managing buildpacks.

## buildpacks:install

Usage: `plushu buildpacks:install <remote> [local]`

Installs a buildpack by cloning the named remote into the `buildpacks`
directory. The remote repository can be specified as a GitHub username/project
combo.

By default, the name the buildpack will be installed to is the same as the
repository name.

## buildpacks:uninstall

Usage: `plushu buildpacks:uninstall <buildpack>`

Removes the buildpack's directory.

## Installing buildpacks from a list

```bash
while read buildpack; do
  plushu buildpacks:install $buildpack
done < buildpacks.txt
```
