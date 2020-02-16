# three-voxel-loader

> [three.js](https://github.com/mrdoob/three.js) plugin for loading voxel data

[![npm version](http://img.shields.io/npm/v/three-voxel-loader.svg?style=flat)](https://npmjs.org/package/three-voxel-loader "View this project on npm")
[![Build Status](https://travis-ci.org/andstor/three-voxel-loader.svg?branch=master)](https://travis-ci.org/andstor/three-voxel-loader)
[![Coverage Status](https://coveralls.io/repos/github/andstor/three-voxel-loader/badge.svg?branch=master)](https://coveralls.io/github/andstor/three-voxel-loader?branch=master)
[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/andstorh/three-voxel-loader.svg?)](https://lgtm.com/projects/g/andstorh/three-voxel-loader/context:javascript)

Documentation - Wiki

## Table of Contents
  * [Installation](#installation)
  * [Usage](#usage)
  * [Import support](#import-support)
  * [License](#license)

## Installation
This library requires the peer dependency [three.js](https://github.com/mrdoob/three.js/).

```sh
$ npm install --save three
```

```sh
$ npm install --save three-voxel-loader
```

## Usage

### Syntax
```js
new VoxelLoader()
```

### Example
```js
const VoxelLoader = require('three-voxel-loader');

// Instantiate the loader
let loader = new VoxelLoader();

// Load a resource from provided URL.
loader.load(
	// Resource URL.
	'models/monster.vox',

  // Called when resource is loaded.
  function ( voxels ) {
		scene.add( voxels );
	},

  // Called when loading is in progresses.
	function ( xhr ) {
		console.log( ( xhr.loaded / xhr.total * 100 ) + '% loaded' );
	},

  // Called when loading has errors.
	function ( error ) {
		console.log( 'An error happened' );
	}
);
```

## Import support
Importing of several file types and data structures with voxel data are supported.

### File formats
- VOX
- XML

### Data structures
- 3D array
- [Sparse octree](https://github.com/vanruesc/sparse-octree)

## License

three-voxel-loader is licensed under the [MIT License](https://github.com/andstor/three-voxel-loader/blob/master/LICENSE).
Copyright © [André Storhaug](https://github.com/andstor)
