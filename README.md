# Read Time Counter JS

Read Time Counter is a ***simple and robust*** reading time counter that **accurately** counts words, characters, and images in your content.

It calculates the estimated reading time for English, CKJ (Chinese, Korean, Japanese), and other Latin-based languages by combining text reading and image viewing times.  

&nbsp;

## How to use?

Ways to include the script:

### 1. Directly embed the script

Embed the script on your page, ideally before the closing `</body>` tag, to ensure all elements are loaded before the script runs.

```html
<script>
// Paste the code of readtime.js here
</script>
```

### 2. Host and link your own .js file

Place this in the `<head>` with the `defer` attribute so it runs after the DOM is parsed:

```html
<script defer src="readtime.js"></script>
```

### 3. Use the CDN version

```html
<script defer src="https://cdn.jsdelivr.net/gh/SPACESODA/readtimecounter@3.2.8/readtime.min.js"></script>
```

&nbsp;

## Define the area

Wrap your article content in an element with the attribute `id="readtimearea"`.

**Note:** Only one `readtimearea` is supported per page.

&nbsp;

## Output elements

Display the estimated reading time (in minutes) by adding an element with the `id="readtime"`. For example: `<span id="readtime"></span>`

The script also outputs individual counts for:  
•	**Words:** Displayed in an element with `id="wordCount"`.  
•	**CKJ Characters:** Displayed in an element with `id="ckjCount"`.  
•	**Images:** Displayed in an element with `id="imgCount"`.  
•	**Combined Info:** For displaying a summary, use `id="hybridCount"`.

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

&nbsp;

## Configurations

If you’re using the CDN version, you can override the default reading speed and time format like this:

```html
<script defer src="https://cdn.jsdelivr.net/gh/SPACESODA/readtimecounter@3.2.8/readtime.min.js"></script>
<script>
  window.readingTimeSettings = {
    engSpeed: 225, // words per minute for English
    charSpeed: 300, // characters per minute for CKJ
    imgSpeed: 10, // seconds per image
    timeFormat: "integer" // "decimal" or "integer"
  };
</script>
```

&nbsp;

## Live Example on CodePen

Visit: https://codepen.io/pen/EaxyZzG

📣 **Please feel free to comment, contribute and make the code better!**

&nbsp;

---

References:

https://en.wikipedia.org/wiki/English_alphabet

https://en.wikipedia.org/wiki/CJK_characters

https://en.wikipedia.org/wiki/Universal_Character_Set_characters

&nbsp;
