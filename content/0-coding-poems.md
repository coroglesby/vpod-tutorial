---
title: Coding Poems
nav: true
--- 

# <i style='color:black;' class='fa fa-align-left'></i> Coding Poems

Though every poem is going to be different, the following should provide enough of a guide to get started with most poems. First we'll show how to code a basic poem with no crazy white-space or other visual features - just left-aligned lines and some stanza breaks. Then we'll talk about <a href="#tips">tips and tricks</a> for the trickier poems.

### Basic step-by-step

##### 1. Copy the poem from the PDF or Word doc and paste it into a plain text editor. In this tutorial, we'll be using <a href="https://notepad-plus-plus.org/downloads/">Notepad++</a> (Windows).

##### 2. You'll often need to re-break the lines once in Notepad++ so the pasted poem matches the original.

##### 3. Highlight the space at the end of the first line through to the beginning of the next line down, and type `Ctrl+H`.
{% include figure.html img="coding-1.PNG" alt="Vandal Poem of the Day logo" caption="" width="100%" %}

##### 4. In the Replace field, type `</p>\n<p class="line">` and click `Replace All`. 
{% include figure.html img="coding-2.PNG" alt="Vandal Poem of the Day logo" caption="" width="100%" %}

##### 5. This should make the poem look like this:
{% include figure.html img="coding-3.PNG" alt="Vandal Poem of the Day logo" caption="" width="100%" %}

##### 6. Notice you'll have to add one more `<p class="line">` to the first line, and you'll have to delete the last `<p class="line">` at the end of the poem.

*Also, a quick note on what this code is doing, so far: `<p class="line">` is telling each line of the poem to act like a "line" version of paragraph, which is a class we've defined in the website's custom CSS. This paragraph class is designed to force longer lines in poems to wrap with an indentation on smaller devices. The empty `<p class="line"></p>` throughout the example above are white space placeholders for stanza breaks.*

##### 7. Now, you'll need to add the top and bottom matter to the poem so that author/publisher/UI Library info appears in the post. This code will (pretty much) always look like this:

###### Top matter:

`<p class="line byline"><em> by <a href="http://poetry.lib.uidaho.edu/index.php/poets/#sierra-nelson">Sierra Nelson</a></em></p>&nbsp;`

{% include figure.html img="coding-4.PNG" alt="Vandal Poem of the Day logo" caption="" width="100%" %}

###### Bottom matter:

`<p class="line bookinfo">from <a target="_blank" href="http://www.poetrynw.org/issue-cover/spring-summer-2010/" rel="noopener noreferrer"><em> Poetry Northwest 05.1 Spring & Summer 2010</em></a><a target="_blank" class="librarylink" href="https://alliance-primo.hosted.exlibrisgroup.com/primo-explore/search?query=any,contains,Sierra%20Nelson&tab=everything&search_scope=everything&vid=UID">Find more by  Sierra Nelson at the library</a></p><p class="citation">Copyright © 2010 Sierra Nelson Used with the permission of <a href="http://poetrynw.com/" target="_blank" rel="noopener noreferrer">Poetry Northwest</a>.`

{% include figure.html img="coding-5.PNG" alt="Vandal Poem of the Day logo" caption="" width="100%" %}

##### 8. You'll of course need to make sure the links and author name are all correct.
- The one link in the top matter `<a href="http://poetry.lib.uidaho.edu/index.php/poets/#sierra-nelson">` will take clickers to the author's bio page. 
- In the bottom matter, the first link `<a target="_blank" href="http://www.poetrynw.org/issue-cover/spring-summer-2010/" rel="noopener noreferrer">` points to the book or journal the poem was published in (usually the publisher's website, or another reliable purchasing point for the book).
- The next link `<a target="_blank" class="librarylink" href="https://alliance-primo.hosted.exlibrisgroup.com/primo-explore/search?query=any,contains,Sierra%20Nelson&tab=everything&search_scope=everything&vid=UID">` is the UI Library search link, which you can modify for each author by simply changing the name in the URL.
- The final link `<a href="http://poetrynw.com/" target="_blank" rel="noopener noreferrer">` points to the featured publisher's website homepage.

##### 9. The actual title of the poem will be entered into WordPress when we get there. For now, this basic poem is all ready to go!



(Actually, 10. Check for typos again. And again.)

##### Your coded poem should look something like this: 

{% include figure.html img="coding-6.PNG" alt="Vandal Poem of the Day logo" caption="" width="100%" %}

<hr>

<a id="tips">

### Tips and Tricks for More Difficult Poems

##### Indented lines (white space at the beginning of the line)
- Add `&emsp;` a few times until you get the indentation to about the size it needs to be.
- Or, add padding your `<p class="line">` like this: `<p class="line em7">` (the greater the em#, the greater the padding)

##### Lines with caesuras (white space) in the middle of them 
- Add `&emsp;` a few times until you get the white space to about the size it needs to be.

##### Justified prose poems

- Remove all line breaks, and instead of `<p class="line">`, use `<p class="prose-poem" style="width:75%">`. You can change the percentage sign there until you get the width of the poem to where it needs to be.

##### Poems that spiral, are shaped like hearts, or are otherwise visually experimental
- Call Devin?