# grunt-indent [![Build Status](https://travis-ci.org/stevenbenner/grunt-indent.png)](https://travis-ci.org/stevenbenner/grunt-indent)

> Change the indentation of files.

## Getting Started
This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-indent --save-dev
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-indent');
```

## The "indent" task

### Overview
In your project's Gruntfile, add a section named `indent` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  indent: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    }
  }
})
```

### Options

#### options.style
Type: `String`
Default value: `tab`

The type of indentation to add or remove. The options are `tab` or `space`.

#### options.size
Type: `Number`
Default value: `1`

The number of `options.style` characters in an indent. For example, if you use 2 spaces per indent then you would set `options.style` to `space`, and this to `2`.

#### options.change
Type: `Number`
Default value: `0`

The indentation level change. If this is a positive number it will indent all lines the specified number of times. If this is a negative number it will remove the specified number of indents. If this number is zero then it will merely copy the files without modifying the contents.

### Usage Examples

#### Increase Indentation
In this example the indent task will increase the indent of all .js files in the src directory by one and save the modified files in the dist directory.

```js
grunt.initConfig({
  indent: {
    src: ['src/*.js'],
    dest: 'dist/',
    options: {
      style: 'space',
      size: 2,
      change: 1
    }
  }
})
```

#### Decrease Indentation
In this example the indent task will decrease the indent of all .css files in the css directory by one and save the modified files in the dist directory.

```js
grunt.initConfig({
  indent: {
    src: ['css/*.css'],
    dest: 'dist/',
    options: {
      style: 'space',
      size: 2,
      change: -1
    }
  }
})
```

## Release History
_(Nothing yet)_
