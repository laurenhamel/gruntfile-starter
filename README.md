# Gruntfile Starter

This is a custom starter Gruntfile that relies on a supplementary `package-config.json` file and also assumes that your project has a `package.json` file.

## Folder Structure

When using this Gruntfile and configuration, your project structure should contain the following:

- `src/`

  A folder used for source files. These, along with the files placed in `data/` directory, are the only files that you should edit directly.
  
- `data/`

  A folder used for storing sample data files relevant to the project's development. These, along with the files place in the `src/` directory, are the only files that you should edit directly.
  
- `dev/`

  An auto-generated folder that Grunt will create when using `grunt dev`. This folder is intended for use to preview the project during its development.

- `dist/`

  An auto-generated folder that Grunt will create when using `grunt dist`. This folder is intended to store production-ready files that can be deployed into live environments.

## Package Configurations

The main purpose of the `package-config.json` file is to act as a router for Grunt paths. In addition to this, the `package-config.json` file is also used to dyncamically load projecg dependencies, stylesheets, and scripts.

## Package Dependencies

This Gruntfile uses the following Grunt-specific `npm` modules as dependencies:

- `grunt-contrib-watch`
- `grunt-contrib-jshint`
- `grunt-contrib-sass`
- `grunt-contrib-copy`
- `grunt-contrib-clean`
- `grunt-contrib-uglify`
- `grunt-contrib-cssmin`
- `grunt-babel`
- `grunt-includes`
- `grunt-replace`
- `grunt-copy-deps`
- `grunt-postcss`

## Grunt Tasks

This Gruntfile creates the following key Grunt tasks:

- `dev`

  Used during development, `grunt dev` will generate a `dev/` folder with a working preview of the project as the project is being worked on. The contents of the `dev/` directory is pulled from both `src/` and `data/` folders. Additionally, the `grunt dev` command will launch a watch task that will automatically reload your project as changes are made.

- `dist`

  Used for distribution, `grunt dist` will generate a `dist/` folder with production-ready project files. The contents of the `dist/` directory is generated from both the `src/` and `data/` folders.