# Course Outline
A short course outline for mentors to follow. The goal is to review some of the things they learned during their application process, introduce new HTML/CSS features, and get them comfortable applying these techniques in a more independent fashion.

## Lesson 1 (estimated 2-3 hours)
Review, semantic HTML tags, CSS `background`, CSS cascade, `:hover`/`:focus` states, block `margin`/`padding`/`border`, CSS specificity.

1. Introduce the `index.html` file. Walk through the linked styles and scripts. Indicate where they'll be making changes.
2. Open `stylesheet.css` and perform quick review of selectors, rules and the cascade. Have them set body `background`, `color` and `font-size` to see how it effects the page.
3. Introduce the `<header>` and `<footer>` tags, and the `role="main"` attribute. Also `<nav>`, `<article>` and `<aside role="complementary">`. Ask them to work in pairs to determine where to place these in the `index.html` file.
4. Show how to implement a background image in the jumbotron. Once that's done, ask them to use what they learned about the cascade to make all the text on the jumbotron white. If they use separate selectors for each block of text, encourage them to set the color on the `.jumbotron` instead, so that it cascades to all child elements.
5. Ask them to update the buttons to look like the screenshot, using the color from the logo (`#ce5f31`) for `.btn-primary`. They should make this change for all buttons on the page, not just those in the jumbotron. Once done, introduce the `:hover` and `:focus` selectors, and ask them to change the colors to use `#ef7f52` as the background and `#fff` for the text in these states.
6. Working in pairs, ask them to use what they've learned about `:hover` and `:focus` to make the links in the navigation menu show a red (`#ce5f31`) border during interactions. Check that the nav menu items do not jump around (they'll need a transparent border around links in the base state).
7. Describe how margins, padding and borders effect the size of a block element differently. Ask them to give each navigation menu link a left and right padding, and a left and right margin, of `1em`. Point out the small gap that appears as you move the mouse from left to right across the menu. Ask them to modify the link styles to remove this gap, so that the mouse moves immediately from one link to the next.
8. Ask them to add a margin to the "Learn More" heading, so that there is more space between the jumbotron and the heading. If they apply it to `h2` or `heading-underline`, it will add a top margin to the "Upcoming Events" heading. Ask them to work in pairs to figure out how they can apply this margin to only the "Learn More" header.

### Homework
1. Read about [advanced CSS selectors](http://learn.shayhowe.com/advanced-html-css/complex-selectors/). Try to complete this [CSS Selector game](https://flukeout.github.io/). It gets hard at the end, but try your best!
2. Try to make the articles under "Upcoming Events" look as close to the completed example screenshot as possible. Students should identify inconsistent spacing above and below the second article. They should also make the Facebook events text bold and space out the icon.
2. Read about [HTML forms](http://learn.shayhowe.com/html-css/building-forms/). Try to create a new HTML page, `contact.html`, based off of the example that we've been working with so far. In this page, replace the jumbotron and the "Learn More" section with a contact form. This form should ask the user to enter their name, email address and phone number, and present them with a large area to enter a message. You may use [Bootstrap's input groups](http://getbootstrap.com/components/#input-groups) if you like. But also use the CSS techniques you've learned so far to style this form like the rest of the site. Things like border colors, labels and buttons should fit with the existing style of the page.

### Research and present at the next class
Assign one of the following topics to each student. Presentations should be 5 minutes each.
- HTML aria attributes
- CSS box model
- Vertically centering content
- CSS naming patterns (BEM/OOCSS)
- z-index
- Positioning (absolute, relative, fixed)
- Icon fonts
- CSS transitions


### Prepare for the next class
1. Read this [introduction to media queries](https://varvy.com/mobile/media-queries.html).

## Lesson 2 (estimated 2-3 hours)
The responsive web, media queries, and content positioning.

1. Student presentations with questions and answers.
2. Talk about how the web is viewed on many device widths, and a modern developer has to find a way to display content that looks great on every device.
3. With the developer tools open, have them drag the screen width down to 320px. Point out how the text "Refugees" in the jumbotron exceeds the width of the image. Ask them to reduce the size of the text to `3em`. Now view the webpage in a wider window again, to show how it seems too small on a larger screen.
4. Introduce the following media query and deconstruct each part: `@media screen and (min-width: 480px)`. Using this knowledge, ask them to increase the font size of the "Refugees" text only when a screen is larger than `480px`.
5. Using the techniques they've learned, ask them to make sure that the buttons in the jumbotron fit on one line on small screens. (They should modify the padding and font size, rather than removing or hiding text).
6. Introduce `static` and `relative` positioning ([the difference](http://stackoverflow.com/questions/5011211/difference-between-static-and-relative-positioning)). Point out how elements in the jumbotron appear vertically one after the other, except for the buttons, which appear side by side. Explain the difference between `block` elements and `inline` elements. Ask them to give the buttons within the jumbotron (`.jumbotron .btn`) a `block` display rule to see how they behave differently.
7. Now have them apply an `absolute` position to `.jumbotron .buttons`. Explain how the `.jumbotron` box no longer extends to contain the `.buttons` box. It falls "outside" of the element.
8. Have them give the `.jumbotron .buttons` element `left` or `right` attributes of `0`. It should position them outside of thet jumbotron. Add a `position: relative` to the jumbotron to illustrate how absolute positioning works relative to the closest parent element with `position: relative`.
9. Working in pairs, ask them to use this absolute positioning technique to anchor the buttons ot thebottom of the jumbotron, with each button taking up exactly 50% of the width. This will be a challenging excercise. They'll need to get the absolutely positioned buttons element full width, peg it to the bottom, absolutely position the buttons themselves and then align each one differently. If possible, they should add padding to the bottom of the jumbotron to make room for the buttons and adjust the border radius of the jumbotron so that it doesn't poke out at the corners.
10. Once they've done this, ask them to reset their styles for all devices larger than `480px`, so that all the elements have relative positioning and their other attributes are "reset" (`border-radius`, `left`, `right`, etc.).

### Homework
1. Do the course on [Responsive web design fundamentals](https://www.udacity.com/course/responsive-web-design-fundamentals--ud893). The first lesson has them set up device testing with remote debugging. If you're unable to get this working, or don't have a mobile device to test with, that's ok. Just use the emulator option in your browser's developer tools.
2. Read more about [positioning content in CSS](http://learn.shayhowe.com/html-css/positioning-content/).
3. Using what you've learned about floating elements from the responsive web design fundamentals course, float the two "Learn More" articles side-by-side. Do not use Bootstrap's grid to accomplish this. Try to give the first box a grey background. When checking the homework, make sure they've properly cleared the floats for the parent element, that the grey box has visual padding and that the adjacent boxes are aligned vertically. By the end of this assignment, their page should look like the completed example.
