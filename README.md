# Web Dev Starter Code

## Overview

### Author Info
Justin Mello  
CS 408  
Fall 2024  
Module 2: Lab 2.2  

# Project Description

For this project we were given a site with accessibility issues, and tasked with addressing as many of said issues to the best of our abilities. The site was checked with an accessibility checker, and we practiced navigating a site
from the perspective of a user who would encounter these accessibility challenges.

## Accessibility Lab Answers  

### Color
#### The text is difficult to read because of the current color scheme. Can you do a test of the current color contrast (text/background), report the results of the test, and then fix it by changing the assigned colors?

I did a test in lighthouse for accessibility in general and focused on the background and foreground colors. Almost everything essentially failed as the contrast ratio was very low. I clicked the how to meet color contrast ratios and read through that section. I decided to use a very white background to provide sufficient contrast with the darker text. That boosted the accessibility significantly (over 12%, I had already started fixing some items so it may have been more if I had done this from the get go.)


### Semantic HTML

#### The content is still not very accessible — report on what happens when you try to navigate it using a keyboard.
Navigating using a keyboard is not effective at all. Hitting tab immediately goes to the Search Query (Which could be useful), but tabbing again to navigate just goes to the go button for the search bar, and then skips all of the content altogether to land on the audio file. There are no images navigated to, and the text is skipped completely. I think this would cause significant issues with a screen reader.

#### Can you update the article text to make it easier for screen reader users to navigate?

Yes, we can update the article text by adding in appropriate tags, such as sections within the article text itself, appropriate headings, and paragraph tags which will also remove the need for the `<br>`. In addition to the next question about the `<div class="nav">` I also decided to update the related content with an aside tag to improve the pages structure.

#### The navigation menu part of the site (wrapped in <div class="nav"></div>) could be made more accessible by putting it in a proper HTML semantic element. Which one should it be updated to? Make the update.

This element should be updated to the "nav" html semantic element, which is appropriate for navigation type menu's and better than using a div which does not provide information about the element.

### The Images

#### The images are currently inaccessible to screen reader users. Can you fix this?
Yes, we can fix this by adding appropriate alt text to each image, so that a screen reader user gets the context from the image via the description. This is a good way to provide images for accessibility purposes!

### The Audio Player

#### The `<audio>` player isn't accessible to hearing impaired (deaf) people — can you add some kind of accessible alternative for these users?

Yes, we can add a transcript. Thankfully the clip is short so I could transcribe it myself!
Normally for work we have an official document, but to make it easy here I just made a super basic webpage with the transcribed content that also has a link back to the main page.

This should be navigable for screen readers and anyone hearing impaired, offering slightly more accessibility that the straight up audio file!



#### The `<audio>` player isn't accessible to those using older browsers that don't support HTML audio. How can you allow them to still access the audio?



### The Forms
#### The `<input>` element in the search form at the top could do with a label, but we don't want to add a visible text label that would potentially spoil the design and isn't really needed by sighted users. How can you add a label that is only accessible to screen readers?


#### The two `<input>` elements in the comment form have visible text labels, but they are not unambiguously associated with their labels — how do you achieve this? Note that you'll need to update some of the CSS rule as well.

### The Show/Hide Comment Control
#### The show/hide comment control button is not currently keyboard-accessible. Can you make it keyboard-accessible, both in terms of focusing it using the tab key and activating it using the return key?

### The Table
#### The data table is not currently very accessible — it is hard for screen reader users to associate data rows and columns together, and the table also has no kind of summary to make it clear what it shows. Can you add some features to your HTML to fix this problem?


### Other Considerations?
#### Can you list two more ideas for improvements that would make the website more accessible?

## Sources and Credits

TODO: You must credit the sources and authors of any code, libraries, or other
assets you use in your project. If you leave this section blank, your project
will be considered in violation of the Academic Honesty policy unless you truly
created everything from scratch with no outside help. If you need to use a
source that you cannot credit (e.g. a classmate's work), you must get explicit
permission from your instructor.

A simple bulleted list below is sufficient. For example:

- Bootstrap: https://getbootstrap.com/
- jQuery: https://jquery.com/
- Background image: https://unsplash.com/photos/...
- Sound effects: https://freesound.org/people/...
- Icons: https://fontawesome.com/
- Fonts: https://fonts.google.com/
- etc.