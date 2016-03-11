# INSTALL
```
$ meteor add fourseven:scss
$ meteor add poetic:materialize-scss
$ meteor remove materialize:materialize # if you have materialize installed
```

# SCSS
Add the following lines to your scss file to load the components (E.G. main.scss):
```
@charset "UTF-8";

// Mixins
// @import "{poetic:materialize-scss}/sass/components/prefixer";
@import "{poetic:materialize-scss}/sass/components/mixins";
@import "{poetic:materialize-scss}/sass/components/color";

// Variables;
// A full version of the "_variables.scss" file is available here: https://github.com/Dogfalo/materialize/blob/master/sass/components/_variables.scss 
// Uncomment this line and comment the next one to override the variables file
//@import "overrides/variables";
@import "{poetic:materialize-scss}/sass/components/variables";

// Reset
@import "{poetic:materialize-scss}/sass/components/normalize";

// components
@import "{poetic:materialize-scss}/sass/components/global";
@import "{poetic:materialize-scss}/sass/components/material-icons.scss";
@import "{poetic:materialize-scss}/sass/components/icons-material-design";
@import "{poetic:materialize-scss}/sass/components/grid";
@import "{poetic:materialize-scss}/sass/components/navbar";
@import "{poetic:materialize-scss}/sass/components/roboto";
@import "{poetic:materialize-scss}/sass/components/typography";
@import "{poetic:materialize-scss}/sass/components/cards";
@import "{poetic:materialize-scss}/sass/components/toast";
@import "{poetic:materialize-scss}/sass/components/tabs";
@import "{poetic:materialize-scss}/sass/components/tooltip";
@import "{poetic:materialize-scss}/sass/components/buttons";
@import "{poetic:materialize-scss}/sass/components/dropdown";
@import "{poetic:materialize-scss}/sass/components/waves";
@import "{poetic:materialize-scss}/sass/components/modal";
@import "{poetic:materialize-scss}/sass/components/collapsible";
@import "{poetic:materialize-scss}/sass/components/chips";
@import "{poetic:materialize-scss}/sass/components/materialbox";
@import "{poetic:materialize-scss}/sass/components/form";
@import "{poetic:materialize-scss}/sass/components/table_of_contents";
@import "{poetic:materialize-scss}/sass/components/sideNav";
@import "{poetic:materialize-scss}/sass/components/preloader";
@import "{poetic:materialize-scss}/sass/components/slider";
@import "{poetic:materialize-scss}/sass/components/carousel";
@import "{poetic:materialize-scss}/sass/components/date_picker/default.scss";
@import "{poetic:materialize-scss}/sass/components/date_picker/default.date.scss";
@import "{poetic:materialize-scss}/sass/components/date_picker/default.time.scss";
```

# ICONS
Icons are automatically imported from this package.

You do NOT have to add an additional head element mentioned at http://materializecss.com/icons.html.

Read more about the MaterialIcons at https://google.github.io/material-design-icons/

# JAVASCRIPT
Javascript is automatically imported from this package.

# CHANGE LOG

- 2016-01-28 update to materializecss [0.97.5](https://github.com/Dogfalo/materialize/tree/v0.97.5#changelog)
- 2015-11-22 update to materializecss [0.97.3](https://github.com/Dogfalo/materialize/tree/v0.97.3#changelog)
  - We rewrote the package as a fork and archived the previous gitrop. If you are looking for code in a version lower than 1.97.3, please check the archived [repo](https://github.com/poetic/meteor-materialize-sass-archived). (*Breaking*)

- 2015-10-01 update package for METEOR@1.2 (*Breaking*)
  - fourseven:scss is updated to 3.3.3_1
  - scss.json is not used anymore.
  - index.scss is not autoupdated anymore, you need to manullay update index.scss.

- 2015-06-26 upgrade to [0.97.0](https://github.com/Dogfalo/materialize/tree/v0.97.0#changelog)
  - Icon Change (*Breaking*):

    ```<i class="mdi-content-add"></i>``` is still supported.

    However you should use ```<i class="material-icons">add</i>``` instead as
    metioned in the materialize [doc](http://materializecss.com/icons.html).

# FOR MAINTAINERS

- HOW TO UPDATE TO NEW VERSIONS OF MATERIALIZECSS
```
git checkout master
git pull https://github.com/Dogfalo/materialize.git master --tags
git checkout <previous-mms-version-on-github>
git checkout -b <next-mms-version>
git rebase <latest-stable-materializecss-version>
// check if we need to add new files to package.js
// change meteor package version
// test
meteor publish
```
