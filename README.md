# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

This is a webpage with a QR code for Frontend Mentor's website and some text about it.

### Screenshot

[screenshot](finalproduct/screenshot.png)

### Links

- Solution URLs: [html file](QRcode.html)
[css file](assets/stylesheets/main.css)

## My process

I started with writing the HTML only. I put the image on top of the text. The image was my header. The text was my footer. I used h1 and h4 for my text elements.

I then wrote the CSS. As this is my first project, I went through a bit of trial and error here. I started by resizing the image. I then centered all elements horizontally (more on this in "What I learned"). I then installed and embedded the font. I then added borders, padding, and line heights (more on this in "What I learned"). I then centered all elements vertically (more on this in "What I learned").

### Built with

- HTML
- CSS

### What I learned

I had trouble centering the elements horizontally. At first, I was able to do it by simply aligning the text to the center. At the time, the text was in a body element rather than a footer element, which caused the image to follow the text to the center. But when I changed the width of the text elements, the text went to the left again, while the image stayed in the center. I had to Google how to move elements to the horizontal center, and this is the code that worked.

```
html {
    display: inline-block;
    width: 20%;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
}
```

While adding padding and borders, I realized that the element's box in the browser did not move with the element's contents when padding or borders were added (easily seen with Developer Tools in Chrome). This meant that the alignment of background colors wasn't right. To fix this, I put a div element around the entirety of the header and footer sections and changed the width of the div.

```
div {
    width: 300px;
    /* same width as the image (header), this solved the background of the text (footer) being too small and aligned with the left of the image rather than the center */
    padding: 15px;
    padding-bottom: 30px;
    border: 1px solid #fff;
    border-radius: 20px;
    background-color: #fff;
/*...*/
  }
```

After the div element was added, the webpage looked exactly as it does now, except the elements were only aligned to the center horizontally; they was aligned to the top vertically. I had trouble centering them vertically too, so I Googled solutions and this code is what worked.

```
div {
/*...*/
    position: absolute;
    top: 50%;
    -ms-transform: translateY(-50%);
    transform: translateY(-50%);
  }
```

## Author

- Website - [Nathan Grissett](https://github.com/nathangrissett)
- Frontend Mentor - [@nathangrissett](https://www.frontendmentor.io/profile/nathangrissett)