# Laravel Rot Ebal Framework Patches
A set of patches that fix bugs and improve the functionality of Laravel Framework.

Currently developed, compatible and tested with Laravel Framework 6.6.1.


## Installation

You can install the package in to a Laravel Framework app via composer:

```bash
composer require laravelrotebal/framework-patches
```

All patches will be applied automatically!


## Why is this package needed?

- [x] Core bug fixes.
- [x] Core improved functioning.
- [x] Core smell code correction.
- [x] More flexible core code for best practices.


## TODO

- [ ] Manually choose which patches to apply.
- [ ] Create tests for testing patched functionality.
- [ ] Compatible with other versions of Laravel Framework.
- [ ] Uniform naming of patches.


## Depends on the package vaimo/composer-patches

Applies a patch from a local or remote file to any package that is part of a given composer project. Patches can be defined both on project and on package level. Optional support for patch versioning, sequencing, custom patch applier configuration and composer command for testing/troubleshooting patches.


## How it works

Directory `patches/laravel/framework` contains patch files. One patch file for one bugfix or feature improvement.

Section `$.extra.patches.laravel/framework` in `composer.json` contains the patch files to be applied in the specified order.

After run `install`, `require`, `update`, `patch:redo`, `patch:undo` commands of `composer` the specified patches will be applied to the specified packages in the `vendor` directory.


## Patch list


### macroable-call-parent-__call.patch

Macroable trait now work with Models.

Affected files:

- src/Illuminate/Support/Traits/Macroable.php


### has-attributes-are-macroable.patch

Some fixes eloquent magic for use macroable. 

Affected files:

- src/Illuminate/Database/Eloquent/Concerns/HasAttributes.php


### macroable-has-relationships-belongs-to.patch

Some fixes eloquent magic for use macroable. 

Affected files:

- src/Illuminate/Database/Eloquent/Concerns/HasRelationships.php
