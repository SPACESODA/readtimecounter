# Read Time Counter

Read Time Counter is a ***simple and robust*** reading time counter that **accurately** counts words, characters, and images in your content. It calculates the estimated reading time for English, CKJ (Chinese, Korean, Japanese), and other Latin-based languages by combining text reading and image viewing times.  

<br>

## How to use?

There are three ways to include the script:

### 1. Directly embed the script

```html
<script>
  // Paste the code of readtime.js here
</script>
```

### 2. Host and link your own .js file

Include the script on your page, ideally inside the `<head>` tag with the `defer` attribute so it runs after the HTML is parsed.

```html
<script defer src="readtime.js"></script>
```

### 3. Use the CDN

```html
<script defer src="https://cdn.jsdelivr.net/gh/SPACESODA/readtimecounter/readtime.min.js"></script>
```

<br>

## Define the area

Wrap your article content in an element with the attribute `id="readtimearea"`.

**Note:** Only one `readtimearea` is supported per page.

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

<br>

## Configurations

You can override default reading speed and time format by:

```html
<script defer src="https://cdn.jsdelivr.net/gh/SPACESODA/readtimecounter/readtime.min.js"></script>
<script>
  window.readingTimeSettings = {
    engSpeed: 225, // words per minute for English and Latin-based languages
    charSpeed: 300, // characters per minute for CKJ
    imgSpeed: 10, // seconds per image
    timeFormat: "integer" // "decimal" or "integer"
  };
</script>
```

<br>

## Live Example on CodePen

Visit: https://codepen.io/pen/EaxyZzG

📣 **Please feel free to comment, contribute and make the code better!**

<br>

---

References:

https://en.wikipedia.org/wiki/English_alphabet

https://en.wikipedia.org/wiki/CJK_characters

https://en.wikipedia.org/wiki/Universal_Character_Set_characters
