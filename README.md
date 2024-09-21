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

## Running the Website

1. To run everything you will need to Fork or Clone this repository and open in up in an IDE on your local PC or in VS Codespaces.

2. Once you have cloned the Repo, open it up in VS Code.

3. Select the index.html file from the Explorer Window.

4. Then, using the VS Code Command Palette, type: > Live Preview Start Server. If this command is not available, you may need to install the VS Code Live Preview extension.

5. This will open up a website preview within your IDE. You can also open this in an external browser if you choose, by clicking on the 3 horizontal lines icon to the top right of the preview window and selecting 'Open in Browser'.


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

For those using an older browser that doesn't support HTML audio, we can provide them with a direct link to the file. That way they can still access the audio (or video content) being rendered on the page!

### The Forms
#### The `<input>` element in the search form at the top could do with a label, but we don't want to add a visible text label that would potentially spoil the design and isn't really needed by sighted users. How can you add a label that is only accessible to screen readers?

I can do a couple things, I can add a role to the form which will inform screen readers the actual role of the form. I can also add an aria-label which will specifically call out that label to someone using a screen reader, but does not change the visual display of the form so it only appears to those navigating the screen via a screen reader!


#### The two `<input>` elements in the comment form have visible text labels, but they are not unambiguously associated with their labels — how do you achieve this? Note that you'll need to update some of the CSS rule as well.
If I'm understanding this one correctly, we can do this just by updating the labels and applying them correctly with a name label and comment label for each field.

### The Show/Hide Comment Control
#### The show/hide comment control button is not currently keyboard-accessible. Can you make it keyboard-accessible, both in terms of focusing it using the tab key and activating it using the return key?

Yes, we can make this keyboard accessible using a button. Updating it as a button inherently making that accessible versus the current div class that is in! Tested and verified working.

### The Table

#### The data table is not currently very accessible — it is hard for screen reader users to associate data rows and columns together, and the table also has no kind of summary to make it clear what it shows. Can you add some features to your HTML to fix this problem?

Yes, we can add a table summary, table columns, and table row information so that it is clear to the screen reader what is going on in the table!


### Other Considerations?
#### Can you list two more ideas for improvements that would make the website more accessible?

Yes - a couple ideas. I still have some contrast issues with the Header so I could make that text darker still for a better contrast ratio.
I could also use some additional items like tab order, skipping links in the nav menu (or in the audio player) to improve keyboard naviagation. Lastly I suck with alt text so I think the alt text for the images could be improved, and maybe even some captions added!

## Sources and Credits


- [Buttons](https://govtnz.github.io/web-a11y-guidance/wct/buttons/make-a-button-accessible/buttons-keyboard-mouse-and-touch-accessibility.html#:~:text=Native%20HTML%20buttons,-%C2%A7Copy%20link&text=to%20this%20section-,A%20button%20created%20using%20the%20or,the%20Space%20or%20Enter%20keys.)
- HTML Accessibility: https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML
- WAI-ARIA Basics: https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics
- Accessible Multimedia: https://developer.mozilla.org/en-US/docs/Learn/Accessibility/Multimedia
- HTML Tables: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table