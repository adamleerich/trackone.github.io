# trackone.github.io

TrackOne band's website!


## Reference material

* https://jekyllrb.com/docs/variables/
* https://www.fabriziomusacchio.com/blog/2021-08-12-Liquid_Cheat_Sheet/



## Rules for each post

* Front matter
    + `title`
    + `date` -- posts use `date` as the subtitle, pages use `subtitle`
    + `description` or `excerpt`.  Used (with same order of preference) in sending decription to social serivces. If provided, an excerpt will appear with the `header_image` on the home page
    + (Optional) `header_image` following image guidelines below

## Image notes

Dimensions come from inspecting Journal demo page on Sticker laptop with 1920x1080 resolution.

* Header background = 471x707, 2:3 aspect ratio
* Featured images in list of posts on home page = 943x531, 16:9 aspect ratio
* When using the same image for both, only the middle 6/16 = 37.5% of the image is used in the header background

### Website guidelines:

* Header background only: set to 480x720, 2:3 aspect
* Featured image in post: set to 1280x720, 16:9 aspect
* Make sure middle 37.5% of the image is worth highlighting!
* Standard images: 400x400

### Instagram guidelines:

* Landscape = 1080x566, 1.91:1 aspect
* Portrait = 1080x1350, 4:5 aspect
* Square = 1080x1080

### Image galleries:

```
<div class="gallery" data-columns="3">
    <img src="/images/demo/post-05.jpg">
    <img src="/images/demo/post-06.jpg">
    <img src="/images/demo/post-07.jpg">
    <img src="/images/demo/post-08.jpg">
    <img src="/images/demo/post-09.jpg">
</div>
```

### Image carousels

Same as a 1-column gallery.

```
<div class="gallery" data-columns="1">
  <img src="/images/demo/demo-landscape.jpg">
  <img src="/images/demo/demo-landscape-2.jpg">
</div>
```


### Embedded videos

```
<iframe src="https://player.vimeo.com/video/203710832" width="640" height="288" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
```

## Other snippets

### Links as text


```
<a href="https://jekyllthemes.io/theme/journal-personal-jekyll-theme" class="button button--large">Get This Theme</a>
```






# Journal by JekyllThemes.io – Instructions

If you have any questions or feedback about the theme, don't hesitate to reach out to hello@jekyllthemes.io for 1-to-1 support direct from the developers.

---

## Getting started

Copy the theme files to your website directory.

To run the theme locally, navigate to the theme directory in your terminal and run `bundle install` to install the theme's dependencies. Then run `jekyll serve` to start the Jekyll server.

---

## Jekyll basics

If you're not familiar with how Jekyll works, check out [jekyllrb.com](https://jekyllrb.com/) for all the details,
or read up on just the basics of [front matter](https://jekyllrb.com/docs/frontmatter/), [writing posts](https://jekyllrb.com/docs/posts/), and [creating pages](https://jekyllrb.com/docs/pages/).

---

## Customizing the theme

Index comes packed with lots of options to let you customize the theme.

---

### The `_config.yml` file

The main things you might need to change here are:

`site: Journal Jekyll Theme` – change this to your website's name

`url:` – the full URL that your site will be hosted at, e.g. https://your-domain.com

`baseurl:` – add a base URL here if you will be publishing the site inside a folder, e.g. https://your-domain.com/project/ – or if you're hosting it as a 'project page' on GitHub Pages. Example: `baseurl: /project`

When using baseurl, you should reference images in your post/project Frontmatter **without** the baseurl, e.g. `/images/image.jpg` but images inside the Markdown content **should include** the baseurl snippet, e.g. `{{site.baseurl}}/images/image.jpg`

`paginate: 6` – change this to set the number of blog posts on each page

You can also change more advanced things here like the path names, collections etc. You do not need to change any of these to achieve the same look as the demo, so best to leave everything else unless you are confident.

---

### The `settings.yml` file

You'll find this inside the `_data` folder – this is where you can set all of the theme options.

**Basic settings**

`site_title` – change this to your website's title. This shows up in the browser's title bar, and in the sidebar.
`site_tagline` – change this to be a description of your site. This shows up under the title/logo in the sidebar.
`favicon_image` – change this to the location of your favicon image, which shows up in the browser's title bar.

**Header settings**

`logo_image` – if you'd like to use a logo instead of plain text title in your sidebar, enter the link to it here.
`logo_width` – set the width (in pixels) that your logo should appear at. This is useful for adding retina display support – for example if your original image is 400px wide, you could set this value to `200` to display a retina-ready image.
`overlay_opacity` – this sets the opacity of the sidebar overlay, and when you hover over portfolio items. Use a decimal value here, e.g. `0.8` will give you 80% opacity.

**Menu settings**

This allows you to set the links inside your menu. Add each one as a list item with a `title` and `url`. When hosting on GitHub Pages, make sure you leave a trailing `/` at the end of links to category pages (e.g. `/blog/` or `/projects/`).

**Grid settings**

`grid_spacing` – this sets the amount of spacing (in pixels) between each item in grid image galleries.

**Contact settings**

The theme comes with a pre-made contact form that you can use with [Formspree](https://formspree.io/create/jekyllthemes), which is free for up to 50 submissions per month. They also have two great paid plans that offer advanced features. Use the link above to set up your account and then paste the 'endpoint' integration code into the theme settings:

`form_action` – this is the form endpoint attribute that you get from FormSpree, for example `https://formspree.io/abcdefgh`
`confirmation_url` – by default the user is shown a default Formspree thank you page. If you have a premium plan, you can use this setting to provide an alternative URL for that page, for example `/thanks` – we have included a basic thank you page with the theme.
`email_subject` – choose the subject of the email you receive from Formspree.
`send_button_text` – change the text used on the form submit button.

Hint: you can add the contact form to any page of your site using the include – `{% include contact-form.html %}` – for example if you wanted to have the contact form on your About page.

**Social settings**

Here you can add links to your profiles on social networks, and they'll be shown in the sidebar. Simply add your URL next to the ones you want to show.

**Color settings**

Here you can set all the different colors used by the theme. Try them out and find the color pallette that works for you!

**Font settings**

`font_embed` – add an embed code from an external font service. This allows you to use services like Google Fonts or Typekit.
`title_font` – set the CSS name for the font used on titles.
`body_font` – set the CSS anme for the font used for body text.
`regular_weight` – set the font weight for regular styled text.
`bold_weight` – set the font weight for bold styled text.

Below these options, you'll see options for each typographical element used in the theme. For each, you can set the following options:

`small_size` – the size (in pixels) used for this element on small size screens like mobile phones.
`medium_size` – the size (in pixels) used for this element on medium size screens like tablets.
`large_size` – the size (in pixels) used for this element on largers screens like laptops and desktops.
`weight` – the font weight for this element.
`letter_spacing` – the letter spacing (in ems) for this element.
`line_height` – the line-height (in decimals) for this element.

**Advanced options**

`ajax_loading` – use `true` to enable Ajax loading throughout your site. Use `false` to disable it and load pages normally – this can be helpful if you're adding plugins or other javascript to your pages.
`analytics_code` – use this option to add your Google Analytics code.
`custom_styles` – use this option to add custom CSS styles to the theme.
`header_js` – use this option to insert javascript into the header of the page.
`footer_js` – use this option to insert javascript at the end of the page.

---

### Images

Inside the `/images/` folder you'll find a few images included with the theme.

The images in the `/demo/` subfolder are used in the demo project, post and page – you can delete those if you don't need them.

`favicon.png` – you should replace this with the favicon image you'd like to use for your website.

---

## Main pages

The theme comes with some pages set up ready for your content.

### The home page – `/index.html`

This is your website home page, showing your latest blog posts. You can edit some details in the Front Matter at the top of the page:

`title` – this sets the page title, which shows up in the browser's title bar and on search engine results, social shares etc.
`description` – this sets the page meta description, which shows up on search engine results, social shares etc.
`header_image` – this sets the page meta image, which shows up on social shares.

### The projects page – `/projects/index.html`

This is the blog listing page, which shows all your project posts. You can edit the same things as on the home page to customise it for your website, and also a `subtitle` field below the main page title.

---

## Projects, posts and pages

These control the main content of your website, and are found inside the `_projects`, `_posts` and `_pages` folders.

Take a look at the demo content inside each folder for full descriptions on what you can do inside these, and to use as a template for your own content.

---

## Any questions?

If you have any questions or feedback about the theme, don't hesitate to reach out to hello@jekyllthemes.io for 1-to-1 support direct from the developers!

🤘




# Appendix

## HTML classes list

ajax-loading
blog
single
blog-post
blog-post__content
blog-post__header
blog-post__image
blog-post__subtitle
blog-post__title
button
button--large
contact-form
contact-form__gotcha
contact-form__input
contact-form__item
contact-form__label
contact-form__textarea
fab
fa-angle-right
fa-angle-left
fluidbox__ghost
footer
footer__copyright
gallery
gallery__item
gallery__wrap
header
header__content
header__logo
header__logo__img
header__tagline
header__title
header-image
header-image--on
header-overlay
hero__text
image-wrap
intro
loader
loading
menu
menu__list
menu__list__item
menu__list__item__link
menu__toggle
js-menu-toggle
menu__toggle__icon
menu__wrap
no-js
page
page__content
page-loader
pagination
pagination__next
pagination__prev
portfolio
portfolio-item
portfolio-item__content
portfolio-item__image
portfolio-item__info
portfolio-item__link
portfolio-item__subtitle
portfolio-item__title
socials
socials__item
socials__item__link
table-wrap
video-wrap
wrap





