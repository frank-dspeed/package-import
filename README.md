# package-import
Mainly used in NodeJS like environments that use yarn or npm or anything else as wrapper to install packages on import

it is a import helper that uses typescript-rollup as loader to resolve dependencies that get imported.

## Main Goals
Should be able to check if a package exists already and is installed. offering plugins like pnp, rollup, yarn, npm, typescript

## Where it is used?
- open-pwa
- typescript-rollup

## Usage

```
import packageImport from 'package-import'
const resloveMethod = 'resolve','import.meta', 'typescript'
// the 3 is optional and is a baseUrl
// packageImport('name','resolve', './') => Promise<resolvedImport | Promise<rejected>
packageImport('name','resolve', './').then(url => import(url)).catch(e => 'npm install name')

```
