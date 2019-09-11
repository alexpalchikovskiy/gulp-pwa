# gulp-pwa
Progressive Web Application manifest and all META tags with Gulp

## Install

```
npm i gulp-pwa --save
```

## Usage example

```
cosnt gulp = require( 'gulp' );
const pwa = require( 'gulp-pwa' );

const options = {
  srcDir: 'images/pwa',
  name: 'My Application',
  theme_color: '#9cff03',
  background_color: '#9cff03'
}

gulp.task( 'build', () => {
  return gulp.src( 'html/**/*.html' ).pipe( pwa( options ) ).pipe(gulp.dest( 'dist' ));
} );

```

In *dist* directory will add manifest.json and in *index.html* will add all tags which need for PWA.

## Options

**srcDir** - folder or URL where was your icons and splashscreen images.

**name** - application name

**theme_color** - statusbar color (only Android)

**background_color** - background color when launching app (only Android, because iOS use splashscreen image)

[More options](https://github.com/alexpalchikovskiy/pwa-config/blob/master/README.md)

## Important

All icon names must be **icon-${size}x${size}.png** (as example icon-540x540.png)

All splashscreen names must be **splashscreen-${width}x${height}.png** (as example splashscreen-1242x2688.png)

[Full list of icons and splashscreens](https://github.com/alexpalchikovskiy/pwa-config/blob/master/README.md)
