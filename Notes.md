Paragraphs: `<p> and </p>`
Used for blocks of text, the body

Headlines: `<h1> and </h1>` through to `<h6> and </h6>`
Used to frame importance of information
#### Italics:
- for visual difference compared to rest of the text only: `<i> and </i>`
- for emphasis: `<em> and </em>`
#### Bold:
- For visual difference only: `<b> and </b>`
- for importance, seriousness, urgency: `<strong> and </strong>`
Even though there is no visual difference, these differences are important when screen readers are used
#### Lists:
- Teasers
- Navigation
- **Unordered**:
	- Most common
	- list item`<li> and </li>`
	- Unordered list `<ul> and </ul>`
	- List items go within unordered lists
- **Ordered**:
	- instead of `<ul> and </ul>`, you use `<ol> and </ol`
	- It's just a different wrapping element
	- Numbered/counted list
- **Definition/description**:
	- Term is `<dt> and </dt>`
	- definition/description of the term is `<dd> and </dd>`
	- you can have >1 dd for 1 dt
	- All of this is wrapped in `<dl>and </dl>` for definition list
#### Quote:
- `<cite> and </cite>` for citing and credits
- `<blockquote> and </blockquote>` to separate from surrounding
- For in text quote `<q> and </q>`

#### Dates and Time:
- `<time> and </time>` 
- HTML attribute for time: 
	- `<elementname attributename="">
	- For date: `<time datetime= "2025-05-08"> May 8, 2025 </time>`
	- Dates should be formatted as YYYY-MM-DD
	- For time: `time datetime= "20:15"> 8:15 pm </time>`
	- Time should be formatted as hh-mm-ss.ddd or hh-mm-ss.ddd+hh:mm for time zone
	- If both together, then date before time
#### Code, pre, and br:
- Code:
	- `<code> and </code>` to make text time line look like code
	- If you want to write about HTML but not execute it (so what I am doing right now), you do `<code>&lt:H4&gt:</code>`, this doesn't work in obsidian :(
- Usually line breaks, spaces, indentations are ignored
- Line break:
	- So use `<br>` for line break 
	- no closing tag
	- at the end of each line
	- only breaks line
- Pre elements
	- for indentations and line breaks
	- Wrap text in `<pre> and </pre>`
	- Pays attention to everything
- Pre and code are often used together to show code
#### Super/Sub Scripts, and Small Text:
- Math ML for maths
- Subscript:
	- For chemistry type stuff
	- `<sub> and </sub>`
- Superscript:
	- Indices type stuff
	- `<sup> and </sup>`
- Small Text:
	- eg copyright info
	- Used to mark small importance, not just for visuals (you use CSS for visual details)
	- `<small> and </small>`

#### Attributes:
- Seen before with date and time
- Global attributes can be applied to any HTML element 
- Class Attribute:
	- Targets all elements with that class in CSS or JavaScript
	- E.g. `<p class="intro"> and </p>`
- ID Attribute:
	- Targets unique element with that ID in CSS or JavaScript
	- `<p class="intro" id="article-intro"> and </p>`
#### ARIA Roles:
- Ideally, don't need one
- Makes sites more/fully accessible
- HTML -> DOM Tree -> Accessibility Tree
#### Formatting:
- Unless dealt with specially, more than 1 space will be ignored
- Comments `<!-- (add comments) -->`
- Modern only use lowercase tags
#### Weird Characters:
- `&copy;` for ©
- `&trade;` for ™
- `&star;` for ☆
- Non breaking space:
	- Keeps things together
	- Keeps on the same line
	- `&nbsp;`
	- You can have 2 spaces between each statement if before/after non breaking space
#### Links:
- To make a link `<a href="page.html"> Link </a>`
- Can be done in line, or wrapped around an image
- The link put in is called "absolute URL" as it's a specific spot on the web
- Must have http:// or https://
- HTTP:
	- Hypertext Transport Protocol
	- S is secure
#### URL Paths:
- When it's just a different page on the same website
- it's the /stuff, stuff being the subsections on a website
- Order of the stuff after slash dictates what goes under what
- Trailing / doesn't matter
#### Navigation:
- You can use `<nav> and </nav>`, `<ul> and </ul>`, `<li> and </li>`, and `<a> and </a>`
- You can use classes to format/group it conveniently
- And role and aria label for visual and auditory differentiation and give context
#### Images:
- `<img src-"image.jpg">`, src being source attribute, what image file to load
- `<img src-"image.jpg" alt="black dog">`, alt acts as substitute when image not seen, e.g. screen readers
	- if no description needed, write as `alt=""` so that file name isn't read out loud instead
- `<img src-"image.jpg" alt="black dog" width="400" height="300">` is for size of image
	- It will work without size info, but takes more time
#### Image Formats:
- Goal is high quality AND small file size
- 4 main formats:
	- GIF:
		- Compresses large area of single colour well
		- 256 colours
		- transparency with jagged edges
		- Multiples frames for little movie
	- SVG:
		- Scalable Vector Graphic
		- Logos, icons, etc.
		- Vector file (instruction for drawings), no pixels so very small file size
	- JPG:
		- Compressing photos
		- don't stick to big sizes, makes sites very slow
		- Reliable way of adding photos
	- PNG:
		- Images that need transparency
		- Good compressions
		- Photos and images
		- Depends on use case
#### Responsive Images:
- Difference between big screens like desktops to phone screens
- So deliver different image systems to different screen sizes/platforms
- Does this using operating system, device hardware capabilities, and network speed
- Browser looks at screen density 
- `scrset = "(different links seperated by ,)"` for the different ratios
- Responsive Width:
	- Takes viewpoint and density into consideration
	- Fast
- Also look at responsive pictures
#### Figure and Figcaption:
- Wrap caption with `<figcaption> and </figcaption>`
- wrap caption and image in `<figure> and </figure>`
- More context about the specific graphic/image
#### Audio:
- `<audio controls src="audio.mp3"> </audio>` Gives controls like pause/play and volume
- `<audio src="audio.mp3" loop></audio>` loops the audio
- `<audio src="audio.mp3" autoplay></audio>` plays when page is loaded automatically
- `<source src=.... type = "audio/ogg; codec=opus>` with other file type, must be nested in audio tags
#### Video:
- `<video src="..mp4" controls> </video>`
- Using H.264 codec currently has the widest support across browsers
	- Widely used
	- Not open source
	- Paid
- AV1 is free
#### Captions & Subtitles:
- Use Web Video Text Tracks (WVTT)
- `<track src="(link to stuff).vtt`
  `kind = "caption"`
  `srclang="eg"`
  `default>`
- `kind = "chapters"` lets you jump through video
#### Embedding Other Medio through iframes:
- Embedding: One site content on other site 
- On YouTube:
	- When you try to share a video it gives option to embed
	- Copy pasting that is all that is required
- There can be security concerns (only a real issue when business or very complicated purposes)
#### Supporting Languages:
- `<html lang="en-GB"`
  `...`
  `/html`
- `lang` Attribute:
	- Language
	- Script
	- Alphabet
	- Universal attribute
- If more than 1 language, use `<span lang="(language)"> and </span>`
- Specify flow of language with `dir` attribute
	- `dir="rtl` for (right to) left, `die="ltr"` for (left to) right
- `charset` attribute for script
- ASCII for European languages
- Unicode (UTF-8) for universal
	- `<meta charset="UTF-8">`
	- Wrapped with headers/paragraph
#### Div and Span:
- You can wrap anything in div to make it different section, but it's bad
- `<div>` is block-level
	- eg. Grouping multiple paragraphs
- `<span>` is inline level
	- eg. different language to the rest
- Global Attributes:
	- class
	- id
	- lang
	- aria roles
#### The HTML Page:
- URLs are always involved
- URL -> Request -> HTML
- HTML File:
	- First file returned when request
	- Browser reads whole file and executes
	- Must start with `doctype`:
		- Which era HTML file is from
		- Wrap everything on page `!doctype html> and </html>`
		- `<!doctype html>`
		  `<html lang="en-GB" dir="ltr">`
		  `...`
		  `</html>`
	- `head` element:
		- for meta data and info on document 
		- not to be displayed
	- `body` element:
		- Content
		- to be displayed
#### Document Head/`head` Element:
- Not to be seen by users
- information for browsers
- Meta data:
	- To define settings
	- eg. when you share a link and it turns into a card
	- `<meta charset="utf-8">`
- Title:
	- `<title> and </title>` 
	- not for the display
	- Used by browser
		- Name of tab
		- Bookmark
- `link` element:
	- Link to other assets
	- `rel` attribute to define type of asset
	- `href` attribute provides URL to asset
	- Order matters
- `script` element:
	- tells browser to load JavaScript file
	- Goes in the end of HTML file, or end of head
#### Structuring Content:
- `main` element:
	- Wraps around main content
	- once per webpage
- `header` and `footer` elements:
	- `header` is for logo, name, titles etc.
	- `footer` is for links, copy right, info about company etc.
		- sometimes things like sharing links, publication dates
		- can be anywhere, not necessarily the bottom
- `article` element:
	- Long or short article
	- teaser cards
	- tweet/social media post
	- just means "Unit of content" that is usable
- `section` element:
	- Wraps around sections of content
	- eg. long essay broken into smaller parts
	- zones on websites
	- "Lets just start with another thing"
- `aside` element:
	- To the side/not main attraction
	- eg. side panel, inset panel for additional into, ads
- These aren't necessarily for the position on a page, but more about conveying the meaning of the positions
#### Form Basics:
- eg. log in, sign up
- Basic:
  `<form action="..." method="get">` GET IS BAD
	  `<label for="name"> Name </label>`
	  `<input name="name" id="name">`
	  `<label for="email"> Email </label>`
	  `<input name="email" id="email">`
	  `<button> Sign Up </button>`
  `</form>`
- Good to connect for accessibility and cross platform uses
- To filter input add `type ="textORemail"` to input tag
- To make enter key work as submit, add `type="submit"` so submit tag
- for the ghost text in input fields, add `placeholder="your ghost text"` to input tag
- `<textarea> and </textarea>` for longer entries
- Look into dates and file attachments
#### Tables:

| Element               | Name         | Purpose                                         | Attribute                 |
| --------------------- | ------------ | ----------------------------------------------- | ------------------------- |
| `<table and </table>` | Table        | Wraps whole table                               |                           |
| `<tr> and </tr>`      | Table row    | Wraps set of element, defining them as same row | colspan, rowspan, headers |
| `<th> and </th>`      | Table header | Header for column                               | colspan, rowspan, scope   |
| `<td> and </td>`      | Table data   | Marks actual data                               |                           |
