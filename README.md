## Base

As you can see this repository is forked off jasper2 template project, you can find more details about changing the template there.

## Maintainance

### Updating the people page
Make changes to `_data/authors.yml`. You can mark people that are graduated with `current: False`, you can have `bio` and `long_bio`, and acceptable values for `section` are   


```
  faculty
  postdoc
  phd
  masters
  undergrad
```


If you enter other values they silently won't show up on people page.

### Updating the website
Number of builds (published updates) per day is limited, so test and check your changes before publishing locally. To do that use `bundle exec jekyll serve`


### Updating styleseets
This is a bit tricky. Jasper2 styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need Node and Gulp installed globally. This is not a part of jekyll compilation pipeline and should be done manually. After the installation, from the theme's root directory:

```bash
$ npm install
$ gulp
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.


### Publishing changes
Just `push` your changes. Travis CI will build and publish changes. I should emphasize that the number of pushes per day is limited, so be careful about the frequency of the changes. You can have multiple commits locally and push them all at once, that's fine. Or better, you can use branches properly instead of pushing everything on master. Pushing on other branches won't trigger the deployment pipeline.


## Thanks


Many thanks to the Ghost team for all the design work. Also many thanks to all contributors,
that help keeping the project alive and updated :smile:


## Copyright & License

Same licence as the one provided by Ghost's team. See Casper's theme [license](GHOST.txt).

Copyright (C) 2015-2018 - Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
