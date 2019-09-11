# gulp-pwa
Progressive Web Application manifest and all META tags with Gulp

## Install

```
npm i gulp-pwa --save
```

## Example

```
cosnt gulp = require( 'gulp' );
const pwa = require( 'gulp-pwa' );

const options = {
  srcDir: 'images/pwa',
  name: 'My Application',
  theme_color: '#9cff03'
}

gulp.task( 'build', () => {
  return gulp.src( 'html/**/*.html' ).pipe( pwa( options ) ).pipe(gulp.dest( 'dist' ));
} );

```

In *dist* directory will add manifest.json and in *index.html* will add all tags which need for PWA.

All icons and images must be in the folder *images/pwa* (**srcDir** property in options).

All icon names must be **icon-${size}x${size}.png**

All splashscreen names must be **splashscreen-${width}x${height}.png**
