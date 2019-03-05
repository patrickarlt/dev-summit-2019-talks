
<!-- .slide: data-background="../template/img/2019/devsummit/bg-1.png" -->

<h1 style="text-align: left; font-size: 80px;">CSS for Geographers</h1>
<p style="text-align: left; font-size: 30px;">Patrick Arlt | <a href="https://twitter.com/patrickarlt">@patrickarlt</a></p>
<p style="text-align: left; font-size: 30px;">Slides | <a href="http://bit.ly/2CF5kQw">http://bit.ly/2CF5kQw</a></p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-6.png" -->

## This talk is all fundamentals.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-6.png" -->

## First Some Notes

Lots of supplemental info in these slides.

Designed to help you keep learning beyond this talk.

Pretty much everything is a link.

Slides <a href="http://bit.ly/2CF5kQw">http://bit.ly/2CF5kQw</a></p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-6.png" -->

## CSS is Hard

* Closer to art then computer science
* Design AND development
* Lots of unintuitive concepts
* It has taken me **years** to amass this knowledge
* Changes somewhat frequently
* Best practices change

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-6.png" -->

## Lets do stuff with CSS!

* Customize Esri Apps
* Use Frameworks
* Build Web Pages
* Make Apps

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-4.png" -->

## Basics

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Where does CSS go?

* Inside a `<style>` tag.
  ```html
  <style>/* Put CSS here*/</style>
  ```
* Inside a `.css` file that is loaded with a `<link>` tag.
  ```html
  <link href="my-css-file.css" rel="stylesheet" type="text/css">
  ```
* In the `<head>` tag of your `.html` files.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### What does CSS look like?

<pre style="font-size: 125%;"><code class="ss">html, body, #map {
  margin: 0;
  width: 100%;
  height: 100%;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Selector

<pre style="font-size: 125%;"><code class="css">html, body, #map&nbsp;&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Declaration

<pre style="font-size: 125%;"><code class="css">html, body, #map {
&nbsp;
&nbsp;
&nbsp;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Property

<pre style="font-size: 125%;"><code class="css">html, body, #map {
  margin:
&nbsp;
&nbsp;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Value

<pre style="font-size: 125%;"><code class="css">html, body, #map {
  margin: 0;
&nbsp;
&nbsp;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Property

<pre style="font-size: 125%;"><code class="css">html, body, #map {
  margin: 0;
  width:
&nbsp;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Value

<pre style="font-size: 125%;"><code class="css">html, body, #map {
  margin: 0;
  width: 100%;
&nbsp;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Property

<pre style="font-size: 125%;"><code class="css">html, body, #map {
  margin: 0;
  width: 100%;
  height:
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Value

<pre style="font-size: 125%;"><code class="css">html, body, #map {
  margin: 0;
  width: 100%;
  height: 100%;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### A CSS Rule

<pre style="font-size: 125%;"><code class="css">html, body, #map {
  margin: 0;
  width: 100%;
  height: 100%;
}</code></pre>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## How does CSS work?

<p class="fragment">The "C" is for Cascading<p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### _Cascading_ Style Sheets

Styles from different sources _cascade_ and coalesce into the final styles for the HTML tags that match their selectors.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### A Typical Cascade

* Browser default stylesheet
* User defined stylesheets
* Stylesheets you include with <code>&lt;link&gt;</code>
* <code>&lt;style&gt;</code> tags
* Inline <code>&lt;style&gt;</code> attributes <code>&lt;div style="..."&gt;</code>
* CSS values with <code>!important</code>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### CSS Specificity

When properties collide specificity determines which property wins.

1. Rules with `!important`
2. Inline styles `<div style="...">`
3. `<style>` and `<link>` tags
4. Selector specificity

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### Selector Specificity

1. `#foo` - `<div id="foo">`
2. `.foo` - `<div class="foo">`
3. `tag` - `<div>`

[CSS Explain](https://josh.github.io/css-explain/)

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

In a specificity tie the last loaded rule wins.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

### In Practice

Right click on something you want to change click "Inspect Element"

[Explore a Storymap](https://story.maps.arcgis.com/apps/Cascade/index.html?appid=46daf1304a0c4ad69a8935c7ed2ab692)

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-6.png" -->

## Lets Build an App!

<img src="app.png" alt="A Simple Mapping App" style="border: none; background: transparent; box-shadow: none;">

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/revage/edit?html,output">Block</a> vs <a href="http://jsbin.com/josuba/edit?html,output">Inline</a></h2>

<ul>
  <li><a href="http://www.impressivewebs.com/difference-block-inline-css/">The Difference Between “Block” and “Inline”</a></li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements">Block-level elements</a></li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements">Inline elements</a></li>
  <li><a href="http://learnlayout.com/display.html">Learn CSS Layout: the "display" property</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/ficatu/edit?html,output">Units</h2>

<ul>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/length">Full unit reference</a></li>
  <li><a href="https://css-tricks.com/the-lengths-of-css/">The Lengths of CSS</a></li>
  <li><a href="http://www.quirksmode.org/css/units-values/">Unit and Values - QuirksMode</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/sawoho/3/edit?html,output">Floats</a></h2>

<ul>
  <li><a href="https://css-tricks.com/all-about-floats/">All About Floats</a></li>
  <li><a href="http://alistapart.com/article/css-floats-101">CSS Floats 101</a></li>
  <li><a href="http://learnlayout.com/float.html">Learn CSS Layout: float</a></li>
</ul>

<p>Bonus Demo: <a href="http://jsbin.com/nisuzu/13/edit?html,output">Problems with Floats</a></p>

<p>Bonus Demo #2: <a href="http://jsbin.com/rowoca/8/edit?html,output">Clearing Floats</a></p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/yufimes/edit?html,output">The Box Model</a></h2>

<ul>
  <li><a href="https://css-tricks.com/the-css-box-model/">The CSS Box Model</a></li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model">Introduction to the CSS box model</a></li>
  <li><a href="http://learnlayout.com/box-model.html">Learn CSS Layout: the box model</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/nodufe/9/edit?html,output">Box Sizing</a></h2>

<ul>
  <li><a href="http://learnlayout.com/box-sizing.html">Learn CSS Layout: box-sizing</a></li>
  <li><a href="http://www.paulirish.com/2012/box-sizing-border-box-ftw/">* { Box-sizing: Border-box } FTW</a></li>
  <li><a href="https://css-tricks.com/box-sizing/">Box Sizing</a></li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing">box-sizing</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/livofev/8/edit?html,output">Flexbox</a></h2>

<ul>
  <li><a href="http://flexboxfroggy.com/">Flexbox Froggy</a></li>
  <li><a href="https://scotch.io/tutorials/a-visual-guide-to-css3-flexbox-properties">A Visual Guide to CSS3 Flexbox Properties</a></li>
  <li><a href="http://learnlayout.com/flexbox.html">Learn CSS Layout: flexbox</a></li>
  <li><a href="http://caniuse.com/#feat=flexbox">Can I Use: flexbox</a></li>
  <li><a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox/">A Complete Guide to Flexbox</a></li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes">Using CSS flexible boxes</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/joziniv/edit?html,output">CSS Grid</a></h2>

<ul>
  <li><a href="http://cssgridgarden.com/">Grid Garden</a></li>
  <li><a href="https://css-tricks.com/snippets/css/complete-guide-grid/">A Complete Guide to Grid</a></li>
    <li><a href="https://gridbyexample.com/">Grid by Example</a></li>
    <li><a href="https://developer.mozilla.org/en-US/docs/Tools/Page_Inspector/How_to/Examine_grid_layouts">Debugging Grid Layouts</a></li>
    <li><a href="https://labs.jensimmons.com/">Intro to CSS Grid: Jen Simmons</a></li>

</ul>

<p><a href="http://jsbin.com/zuwarus/edit?html,output">Bonus Demo: CSS Grid Template Areas</a></p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/pitemo/5/edit">Margin, Padding and Borders</a></h2>

<ul>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing">Mastering margin collapsing</a></li>
  <li><a href="https://css-tricks.com/what-you-should-know-about-collapsing-margins/">What You Should Know About Collapsing Margins</a></li>
  <li><a href="http://stackoverflow.com/a/20624095/449686">Compare block elements to pictures hanging on a wall</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/gibuhe/edit?html,output">Media Queries and Responsive Design</a></h2>

<ul>
  <li><a href="http://mediaqueri.es/">Responsive design gallery</a></li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries">Using media queries</a></li>
  <li><a href="https://css-tricks.com/snippets/css/media-queries-for-standard-devices/">Media Queries for Standard Devices</a></li>
  <li><a href="http://learnlayout.com/media-queries.html">Learn CSS Layout: media queries</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/babiwa/4/edit?html,output">Positioning</a></h2>

<ul>
  <li><a href="http://learnlayout.com/position.html">Learn CSS Layout: position</a></li>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/position">position</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/gerexud/3/edit">Typography (Choosing Fonts)</a></h2>

<ul>
  <li><a href="https://www.google.com/fonts">Google Fonts</a></li>
  <li><a href="http://femmebot.github.io/google-type/">Google Web Fonts Typographic Project</a></li>
  <li><a href="http://fontpair.co/">Font Pair</a></li>
  <li><a href="http://www.labnol.org/internet/best-google-font-combinations/28987/">Font tool roundup</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/dugapa/7/edit">Typography (Sizing Type)</a></h2>

<ul>
  <li><a href="http://type-scale.com/">TypeScale</a></li>
  <li><a href="http://typecast.com/blog/a-more-modern-scale-for-web-typography">A More Modern Scale for Web Typography</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2><a href="http://jsbin.com/jafeza/6/edit?html,output">Adding Color</a></h2>

<ul>
  <li><a href="https://flatuicolors.com/">Flat UI Colors</a></li>
  <li><a href="http://esri.github.io/calcite-web/documentation/color/">Calcite Web Colors</a></li>
  <li><a href="http://jxnblk.com/colorable/demos/matrix/">Color Pairing Matrix</a></li>
  <li><a href="https://color.adobe.com/create/color-wheel/">Adobe Kuler</a></li>
  <li><a href="http://www.colourlovers.com/palettes">Color Lovers</a></li>
</ul>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-4.png" -->

<h2><a href="http://jsbin.com/gixaro/13/edit?html,output">Adding JavaScript</a></h2>

<p><a href="https://jsbin.com/ducimox/1/edit?html">Bonus Demo: w/ CSS Grid</a></p>

<p>~120 lines of CSS, ~30 lines of JS.</p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2>Browser Compatibility</h2>

<p>Sites like <a href="http://caniuse.com/flexbox">Can I Use?</a> or <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/">MDN</a> to check if browsers support a specific property. Sometimes experimental or partially supports CSS properties will require a <code>-webkit-</code>, <code>-moz-</code> or <code>-ms-</code> prefix. Tools like <a href="https://autoprefixer.github.io/">Autoprefixer</a> to add prefixes automatically.</p>
<p><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/@supports"></code>@supports</code></a> was introduced with CSS grid to check for support of new features.</p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

<h2>More Browser Compatibility</h2>

<p>Remember Microsoft only supports IE 11 officially now. All other versions are not supported and might have security bugs.</p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-6.png" -->

## Best Practices

* Keep selectors as simple as possible
* Don't use tools until you are familiar with the basics
* Add tools when you feel limited or want more productivity
* Don't worry so much about browser compatibility
* Watch out for the size of web fonts
* Avoid floats for layout, try using Flexbox and Grid
* You can learn **A LOT** with inspector

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-esri.png" -->

<br><br><br><br><br><br>

Slides at http://bit.ly/2T4zaKJ

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-rating.png" -->
