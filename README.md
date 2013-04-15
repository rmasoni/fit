#FIT

## What's this?

**FIT** is a CSS trick based on [blueimp's jQuery File Upload](https://github.com/blueimp/jQuery-File-Upload) that lets you make almost any element trigger the browser's file upload dialog by hiding an `input[type=file]` inside of it.

It's specially useful for designers that despise the browsers' default `input[type=file]` styles, which as of today cannot be changed.

## How to use

Import **fit.css** into your CSS file, then wrap the `input[type=file]` — together with some text or an icon — in an element with the class `.fit`.

Remember to set the container element to have:

- `position: relative;` or `position: absolute;`
- `display: inline-block;` or `display: block;`

## Example

### HTML

``` html
<span class="upload-button fit">
  <input type="file">
  Upload files
</span>
```

### CSS

``` css
@import "fit.css";

span.upload-button {
  /* Mandatory rules */
  display: inline-block;
  position: relative;

  /* Your rules */
}
```

## Browser Support

This trick has been tested and works properly on the latest **Chrome**, **Safari**, **Mobile Safari**, and **Internet Explorer 9/10**.

**Firefox** unfortunately sets a weird clickable area for the `input[type=file]` that can't be changed. This makes slightly large buttons only partially clickable, so I do not recommended you to use this trick if you need to support this browser.
