v0.1.6 - March 1, 2013
----------------------

### Fixed

  * Do not use instance helpers for environment check. (#79)

v0.1.5 - Feb 12, 2013
----------------------

### Fixed
  *  Stylus 0.7.1 support.

v0.1.4 - Feb 12, 2013
----------------------

### Added
  * Multiple asset hosts support. (#27)

### Fixed
  * Lock stylus to 0.7.0 until 0.7.1 is supported.

v0.1.3 - Feb 3, 2013
----------------------

### Added
  * JRuby 1.9 and 1.8 now supported.

### Fixed:
  * Deal with assets with exact same name but extensions. (#75)
  * Ruby 1.8 support (broken in previous v0.1 releases).

v0.1.2 - Jan 20, 2013
----------------------

### Added:
  * Support for custom cache control headers for packed assets. (#43)

v0.1.1 - Jan 15, 2013
----------------------

### Fixed
  * Added less engine support and test (#69)
  * Support for fonts & other AssetPack.supported_formats file format. (#50)
  * Deal with multiple static files with same name but different extensions (ex. fonts).

v0.1.0 - Jan 14, 2013
----------------------

### Changed
  * Using `file` utility instead `identify` utility. (#26)

### Fixed
  * Deal with different encodings in combined assets. (#47)
  * Serve files with dots in name. (#32, #66)
  * Deal with character encoding issues in ruby 1.8. (#51)
  * Add missing depedency for development unit test. (#63)
  * Deal with binary files copy (ex. images), fix errors like `"\x89" from ASCII-8BIT to UTF-8"`. (#38, #67)

v0.0.11 - Feb 21, 2012
----------------------

### Added:
  * Support for 'prebuild' to build on startup.
  * Support for SVG files.
  * Implement UglifyJS support. (#18)
  * Implement ignored files. (#17)
  * Added support classic-style Sinatra apps. (#22)

### Changed:
  * Built files from 'rake assetpack:build' now match the mtimes of their sources. (#12)
  * Update the readme with a note on SASS compression.
  * Use regular expression route matcher instead of splat pattern for Padrino compatibility. (#19)
  * Made `link` and `script` tags (generated by helpers) be more HTML5-like.

### Fixed:
  * Sinatra >= 1.3.0 compatibility. Use 'public_folder' in Sinatra >=1.3.0. (#25)

v0.0.10 - Sep 18, 2011
----------------------

### Added:
  * Support for 'prebuild' to build on startup.
  * Add UglifyJS support via `js_compression :uglify`. (#18)
  * Ignore '.*' and '_*' files. (#17)
  * Allow specifying of files to be ignored. (#17)

### Changed:
  * Built files from 'rake assetpack:build' now match the mtimes of their
    sources. (#12)
  * Refactor Compressor into separate engine classes.

v0.0.9 - Sep 18, 2011
---------------------

### Fixed:
  * Fixed a bad route terminating issue. (#9)
  * Fix the Rake task when the main App class is in a module. (#11)

### Changed:
  * Use Sinatra's `template_cache`. This makes AssetPack honor Sinatra's
    `reload_templates` setting. (#15)

### Added:
  * Added .htc (IE behavior files) to the list of file formats to be served.
  * Added examples.

v0.0.8 - Sep 06, 2011
---------------------

### Fixed:
  * Fixed the CSS preprocessing bug that gives invalid 'url()' properties to
    non-existing images. (#1)

### Added:
  * Allow adding CSS/JS files that don't exist. (#8)
  * Support any Tilt-compatible CSS or JS engine. (#5)

### Changed:
  * Default to '/assets/x.js' then using assets.css without a path. Inspiration
    from Jammit.
  * Ask browsers to cache assets for 1 month.

### Misc:
  * Add a note on the ImageMagick requirement.
  * Stop the 'img' helper from invoking ImageMagick more times than it needs to.
  * Make "rake test!" abort when it encounters an error.
  * Stylus tests to stub stylus compilation.
  * Added .rvmrc and .sass-cache to gitignore.
  * Allow overridable multiple RVM environments in tests.

v0.0.6 - Aug 30, 2011
---------------------

### Fixed:
  * Redundant entries are now suppressed. (eg, when specifying 
      `['vendor/jquery.js', 'vendor/*.js']`)

### Added:
  * Allow a parameter to the block in the `assets` configuration block.
  * Update README with lots of info.
  * Allow multiple packages in the js and css helpers. (eg, `css :base, :login`)
  * Allow setting options for `js_compression` by passing a hash after it.
  * Make the path parameter in `js` and `css` in the `assets` block optional.

v0.0.5 - Aug 30, 2011
---------------------

### Fixed:
  * Fix build failing when it finds directories.

### Added:
  * Added an example app in `example/`.

v0.0.4 - Aug 30, 2011
---------------------

### Fixed:
  * Ruby 1.8 compatibility. Yay!
  * Fixed images always being square.
  * Assets are now ordered properly.

### Changed:
  * the config format for `js_compression` and family. In your `assets` block, 
  you now have to use `js_compression :closure` instead of `js_compression = 
  :closure`.
  * Use simple CSS compression by default.

v0.0.3 - Aug 30, 2011
---------------------

### Added:
  * Images in CSS defined in `url(...)` params are now cache-busted.
  * Add support for embedded images in CSS.
  * `rake assetpack:build` now also outputs images.

v0.0.2 - Aug 29, 2011
---------------------

### Added:
  * Added the `img` helper.
  * Added support for filetypes used in @font-face.

### Fixed:
  * The gem now installs the correct dependencies.

v0.0.1 - Aug 29, 2011
---------------------

Initial release.