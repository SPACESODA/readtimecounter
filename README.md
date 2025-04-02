# Reading Time Counter v3.2.6

A ***simple and robust*** reading time counter that **accurately** counts words, characters, and images in your content. It calculates the estimated reading time for English, CKJ (Chinese, Korean, Japanese), and other Latin-based languages by combining text reading and image viewing times.  

> ⚠️ **This repo will not be further updated. The project will continue to be maintained at:** [https://github.com/SPACESODA/readtimecounter](https://github.com/SPACESODA/readtimecounter)

<br>

## How to use?

### The script:

Simply include the script `readtime.js` in your page’s **footer** code (before `</body>`) and you’re set. For example, add the following to your webpage:

```html
<script defer src="readtime.js"></script>
```

You can also use the CDN version via jsDelivr:

```html
<script defer src="https://cdn.jsdelivr.net/gh/hypestudiox/readtimecounter/readtime.min.js"></script>
```

### Define the area for the counting the Read Time:

Wrap your article content in a container with the attribute `id="readtimearea"`.

**Limitation:** Only one `readtimearea` per webpage is supported.

### Outputs:

Display the estimated reading time (in minutes) by adding an element with the `id="readtime"`.

For example: `<span id="readtime"></span>`

The script also outputs individual counts for:

•	**Words:** Displayed in an element with `id="wordCount"`.

•	**CKJ Characters:** Displayed in an element with `id="ckjCount"`.

•	**Images:** Displayed in an element with `id="imgCount"`.

•	**Combined Info:** For a summary view, use an element with `id="hybridCount"`.

Example:

```html
<p>This article takes around <span id="readtime"></span> minutes to read.</p>
<p class="note">
  There are
  <span id="wordCount"></span> words,
  <span id="ckjCount"></span> CJK characters, and
  <span id="imgCount"></span> images in this article.
</p>
<p class="note">Summary: <span id="hybridCount"></span></p>
```

<br>

## Configurations

You can override default reading speed and time format by:

```html
<script defer src="https://cdn.jsdelivr.net/gh/hypestudiox/readtimecounter/readtime.min.js"></script>
<script>
  window.readingTimeSettings = {
    engSpeed: 220,
    charSpeed: 300,
    imgSpeed: 10,
    timeFormat: "integer"
  };
</script>
```

<br>

## Live Example

See it on CodePen: https://codepen.io/pen/EaxyZzG

📣 **Please feel free to comment, contribute and make the code better!**


<br>

---

References:

https://en.wikipedia.org/wiki/English_alphabet

https://en.wikipedia.org/wiki/CJK_characters

https://en.wikipedia.org/wiki/Universal_Character_Set_characters
