---
layout:     post
title:      useful npm commands
date:       2019-02-06
summary:    ""
categories: javascript
---

### init package.json file with default options:
<code>npm init -y</code>

### install all packages from the package.json dependencies:
<code>npm install</code>
<br>
example: installing all dependencies after cloning the repo.

### installing a module as global:
<code>npm i -g package_name</code>
<br>
example: packages that can be used in multiple projects, like nodemon.

### installing a module as a dependency:
<code>npm i package_name</code>

### installing a module as a development dependency:
<code>npm i --save-dev package_name</code>
<br>
example: mocha and chai packages.

### update npm itself:
<code>npm install -g npm</code>

### check if any installed package is outdated:
<code>npm outdated</code>
<br>
tip: use the flag __-g__ to check for global packages.

### update packages:
<code>npm update [-g] [package]</code>
<br>
if the flag __-g__ is provided, this command will update all global packages installed; otherwise, all local packages will be updated.

### check for all npm configs:
<code>npm config list -l</code>

### set a npm config variable:
<code>npm config set init-author-name "Nikolas José Rangel"</code>

### delete npm config:
<code>npm config delete init-author-name</code>

### search for packages in npm registry:
<code>npm search package_name</code>

### check for the global packages installed:
<code>npm ls -g --depth=0</code>
<br>
for a more detailed list:
<code>npm ll -g --depth=0</code>

### check for a package's details:
<code>npm ll [-g] package_name</code>

### open package's homepage:
<code>npm home package_name</code>

### open package's repo:
<code>npm repo package_name</code>

### not so useful but :santa:
<code>npm xmas</code>