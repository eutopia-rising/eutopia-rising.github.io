# Eutopia Rising webpage

We are using [Feeling Responsive][1] by [Phlow][2] as basis for the
webpage design. There have been some customizations of the theme
beyond the expected configuration for our specific needs:

* The size of the `#masthead` has been increased in
  `_sass/_07_layout.scss` to accommodate the logo.
* Coded added to the screen size specific sections controlling the masthead to make the body padding increase for small screen sizes.
* Top margin for title increased in `_layouts/page.html` to avoid navbar covering title on small screen sizes: `div` changed class from `t30` to `t50`.
* Code in `_layouts/page.html` has been adjusted to allow the
  directory structure we are trying to use (in particular to allow
  post images to reside in `/path/to/post/images`)
* Code in `_layouts/page.html` has been adjusted to reduce the left
  margin: the class `margin-offset-2` has been removed from the `div`
  if `page.sidebar == NULL`.
* Code in `_includes/footer.html` has been adjusted to adapt to the
  page naming scheme already in use. The `More ›` link in the footer
  now points to `/about/` instead of `/info`.
* `_sass/_02_settings_typography.scss` has been adjusted to include
  old font choices.
* A custom made symbol font has been created to include the Eutopia Rising logo and several additional useful symbols to be available through the `.icon-eutopialogosq` CSS class (would place the logo just before the thing that has that CSS class).


## How do I add a new event?

1. Create a new directory in `/blogs` named for your event.
2. Create a subdirectory `images` in the event directory if you want
   an event image.
3. Create a file `index.md` in the event directory. This is where you
   will write your event text.
4. Start `index.md` with the following:
   ```
   ---
   title: "Your Event Title"
   date: "YYYY-MM-DD"
   event: true
   image:
     title: "images/name-of-event-image.png"
   --- 

   ``` 
   Note: if you don't need an event image, remove the two last
   lines. The line `event: true` is needed for your event to be listed
   on the `/events` page.
5. Write your event content.
6. Add an image into the `images` subdirectory in 2.







 [1]: https://github.com/Phlow/feeling-responsive/
 [2]: https://github.com/Phlow/
