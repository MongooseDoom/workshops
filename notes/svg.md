# SVGs

## Scalable Vector Graphics
SVGs are vector graphics declared using XML.
- Small file sizes
- Scalable without loss in quality

## Browser Support
https://docs.google.com/presentation/d/1CNQLbqC0krocy_fZrM5fZ-YmQ2JgEADRh3qR6RbOOGk/edit#slide=id.g33320a161_00

## Exporting from Illustrator
Object > Artboards > Fit to Selected Art
Do's and Don'ts https://docs.google.com/presentation/d/1CNQLbqC0krocy_fZrM5fZ-YmQ2JgEADRh3qR6RbOOGk/edit#slide=id.g27310e803_1582
Named Layers = IDs

## Optimizing
http://petercollingridge.appspot.com/svg-editor

## Using SVG

### Use as an <img>
Browser Support: http://caniuse.com/#feat=svg-img
Use this method if you don't plan to use CSS or scripting.
	<img src="resources/donut.svg" alt="Tasty Donut"/>

### Use as a background-image
Browser Support: http://caniuse.com/#feat=svg-css
For background-image you'll want to use background-size
    div {
      background-image: url(resources/donut.svg);
      background-size: 100px;
    }

### This is where things get interesting.

### Use Inline
Browser Support: http://caniuse.com/#feat=svg-html5
Pros: No http request, more accessibility
Cons: Ugly

### Using SVG as an <object>
This method is best if you want to use CSS and scripting.
    <object data="resources/donut.svg" type=""></object>
Can use fallbacks

iframe and embed also work but object is recommended

### Using Data URIs
svg syntax <img src='data:image/svg+xml;utf8,...'>
base64 <img alt="" src="data:image/svg+xml;base64,...">

## Using CSS with SVGs

### Using CSS to animate SVGs

## So much more
List other things that can be done with SVGs

## Resources:
http://css-tricks.com/mega-list-svg-information/
http://tympanus.net/codrops/2014/08/19/making-svgs-responsive-with-css/
http://danielmall.com/articles/svg-workflow-for-designers/
http://www.sitepoint.com/add-svg-to-web-page/
http://dbushell.com/2013/02/04/a-primer-to-front-end-svg-hacking/
https://www.youtube.com/watch?v=lf7L8X6ZBu8 - http://slides.com/sarasoueidan/styling-animating-svgs-with-css#/
http://css-tricks.com/lodge/svg/table-of-contents/
https://docs.google.com/presentation/d/1CNQLbqC0krocy_fZrM5fZ-YmQ2JgEADRh3qR6RbOOGk/