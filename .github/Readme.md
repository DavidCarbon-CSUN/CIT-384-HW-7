# Homework 7 (Lab) - Resume Site

In this homework, you’ll continue working on your resume site. You can continue building on from Homework 6 Lab.

1. Update the index.html file
   a. Let's update our projects by adding in the content wrappers. To keep the text from spanning across the whole page, starting with the header. Add the first new `<div class="content-wrap">` just after the header tag. We want to make sure we enclose all of the content, but stay within the sections. It should contain all elements that the header contains.
   
   b. Go back to the CSS now and add in this style in the global section. We're going to keep this style here in the global section, because it's going to be reused throughout the project. Give it a `width: 950px; margin: 0 auto;`.

2. Go back to your HTML and add that content wrapper to the rest of the page.
   a. Add one in the work section right after the section tag. Make sure that the closing tag encloses around the content. So it should be right before the closing section tag.
   
   b. Add one in the education section and also the footer section. Also make sure you keep your HTML indented properly so that you can easily see where your opening and closing tags are.
   
   c. Save work and examine your results in Chrome with different window sizes.
   
   d. To make the content wrapper flexible, but while still setting the width on the content, instead of using a width, we can use `max-width` instead. Let's go back to our CSS file and make that update. In the `.content-wrap` selector, remove the `width` property and add `max-width: 950px;`.

3. Practice with padding and spacing.
   a. Still in the `.content-wrap` selector, add some padding. Use one value: 50 pixels (`padding: 50px;`). By adding padding to the content wrap, all the page sections using this class will have the same amount of padding. This will help to keep your designs more consistent.

   b. You may notice that while we added the same amount of padding around the entire content wrapper, there's a small difference in the amount of space between the top of the wrapper and the bottom. This is because there is margin around the heading element. Remove the margin at the top, so that the wrapper padding is more consistent.

   c. Back in your CSS file, find your `h2` selector, and set the `margin-top` to zero (`margin-top: 0;`). This will remove the margin space just from the top of the element. Save it, refresh it, and check it in the browser.
   
   d. Next, address the white border around the entire page. You can see it on the left, bottom, right side, and top. Just like the spacing between the sections, this is coming from the default margin from the body element, which is why it's wrapping the entire page. In your CSS file, find your `body` selector and set the margin to zero (`margin: 0;`). Now the white space is gone and the background colors span all the way across.
   
   e. Go back to the footer. Add some space between the links. Longer blocks of text are usually easier to read when left-aligned, but since there's not much content here, center-align the text. In your CSS file, use `footer` as your selector and add the property `text-align: center;`. Save it and refresh your browser. By adding `text-align: center` to the footer, all child elements within inherit the style.
   
   f. Back in your HTML file, ensure that the styles are applied only to the links within the footer by adding a class to the div containing all the links. After the `h2` tag that says "Let's Keep in Touch!", add a `<div class="contact-info">`. This div should contain all the anchor tags.
   
   g. Back in the CSS file, create a new declaration block named `.contact-info a`. Apply styles to the links using a descendant selector (`a`) to target the links inside the `contact-info` class. Inside that selector, set the values `padding: 10px; display: inline-block;`. Use `inline-block` because you want these elements to align side by side in a line but also to apply the padding properly like block-level elements.

4. Practice with floats in the header
   a. The first thing to focus on is the profile image. Images can be resized with CSS, but it's best to crop the file to the size you need. The larger the image, the more bandwidth the browser uses to load it. In the CSS, set the width and height of the profile image to 300 pixels.

   b. In the HTML, add a class inside the image tag and name it `profile-img`. This way, you can target only this image in the CSS. Also, add it to the header section in your CSS (`.profile-img`). Inside that selector, set `width: 300px;`. You don't need to set the height because by setting the width, the height automatically adjusts to maintain the aspect ratio of the image. Save the file and check your changes in the browser.

   c. Add one more CSS style to the `.profile-img` selector called `border-radius` and give it a value of 50% (`border-radius: 50%;`). Save it and go back to the browser.

   d. Tighten up the header design by removing some margins. To bring the `h1` name and `h2` tagline closer together, remove the margin from both the `h1` and `h2` headings. In your CSS, go to your `header h1`, `header h2` selector and add `margin: 0;`. Go back to the browser and check your changes.

   e. Float the text around the image by adding `float: left` to the `profile-img` selector.

   f. Add the `overflow` property to the `.content-wrap` selector and use the value `hidden`.

   g. Add a little bit of margin on the right side of your image to put some space between it and the text. In the `profile-img` selector, add `margin-right: 30px;`. Save and check your changes in the browser.

5. Add the box model fix
   a. Add the box model fix using the snippet from the lecture to your CSS file. This goes at the very top of your style sheet in the global section since this style is applied to every single element on the page.

6. Add some columns to your page
   a. The first step is to put a box around all of the text elements to group them as one component. In the HTML file, use a div tag to create the container, as this is only for styling purposes. Add a class as well. We're going to create two columns, so we can call them `column-narrow` and `column-wide`. You'll be using these column styles again to align the content in the work experience section. This will be a reusable style.
   
   b. In the HTML, add a class of `column-narrow` to your img tag.
   
   c. Add a new `<div class="column-wide">` that contains the `h1`, `h2`, and `p` tags in your header section.
   
   d. In your CSS, set the style properties for the newly added `.column-narrow` selector to `width: 30%; float: left; padding-right: 3%; min-height: 175px;`.
   
   e. Set the style properties for the newly added `.column-wide` to `width: 70%; float: left; min-height: 225px;`.
   
   f. Remove or comment out the float and margin values from the `profile-img` selector. Since we'll be using these new global column styles instead to align the content, you can keep the `border-radius: 50%;` property.
   
   g. In your HTML file, add divs and classes to your Work Experience section to apply our new styling.
      i. Add a new `<div class="column-narrow">` that contains the `h3` job title, `p` company name, and `p` date at job tags in your Job Details section.
      ii. Add a new `<div class="column-wide">` that contains the `p` job summary, `p` optional list, and the `ul` tags in your Job Details section.
      iii. Make sure to add that to all your job items.
