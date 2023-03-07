# Module 1 Challenge

## Table of Contents

- [The Challenge](#the-challenge)
- [Things to Consider](#things-to-consider)
- [Links](#links)
- [Screenshots](#screenshots)
- [My Process](#my-process)
- [Continued development](#continued-development)
- [Acknowledgments](#acknowledgments)
- [Contributors](#contributors)

## The Challenge

- Refactor the HTML and CSS code to optimize the web page's accessibility and SEO potential.

---

## Things to Consider

- Improve the codebase for long-term sustainability.

- Test all links to make sure there are no bugs.

- Add alt text to images that require semantic  meaning and descriptions.

- Reorganize and consolidate the CSS to improve the efficiency, maintainability and readability.

- Add helpful comments in the HTML and CSS file.

- Optimize the file sizes of the images.

- Add a descriptive page title.

- Change non-semantic HTML elements for more appropriate sematic HTML elements if possible.

- Follow the ***Scout Rule**.

---

## Links

- [Github Pages Link](https://matthew-millard.github.io/module-01-challenge/)

- [Github Repository](https://github.com/matthew-millard/module-01-challenge)

---

## Screenshots

![Desktop Screenshot - Full](./Develop/assets/Screenshots/Desktop-Full-Screenshot-Horiseon-The-SEO-Experts.png)

![Desktop Screenshot - 768px](./Develop/assets/Screenshots/Desktop-768px-Screenshot-Horiseon-The-SEO-Experts.png.png)

---

## My Process

- Give the web page an accurate and descriptive title.

```HTML
<title>Horiseon | The SEO Experts</title>
```

- Change any HTML elements that carried a non-semantic tag to a more suitable semantic tag depending on its content. Ex.👇

Starter Code:

```HTML
<div class="content">
    <div class="search-engine-optimization">
        <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
        <h2>Search Engine Optimization</h2>
        <p>
            The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
        </p>
    </div>
    <div id="online-reputation-management" class="online-reputation-management">
        <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
        <h2>Online Reputation Management</h2>
        <p>
            The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
        </p>
    </div>
    <div id="social-media-marketing" class="social-media-marketing">
        <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
        <h2>Social Media Marketing</h2>
        <p>
            Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
        </p>
    </div>
</div>
```

Refactored Code:

```HTML
<!-- main content -->
<main class="content">
    <section class="content__container" id="search-engine-optimization">
        <img class="content__image float-left" alt="A note pad containing information on SEO strategies." src="./Develop/assets/images/search-engine-optimization.jpg" />
        <h2 class="content__title">Search Engine Optimization</h2>
        <p>
            The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
        </p>
    </section>

    <section class="content__container" id="online-reputation-management">
        <img class="content__image float-right" alt="A laptop displaying a climbing bar chart with the title - reputation." src="./Develop/assets/images/online-reputation-management.jpg"/>
        <h2 class="content__title">Online Reputation Management</h2>
        <p>
            The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
        </p>
    </section>

    <section class="content__container" id="social-media-marketing" >
        <img class="content__image float-left" alt="Social media marketing experts collaborating around the table." src="./Develop/assets/images/social-media-marketing.jpg"/>
        <h2 class="content__title">Social Media Marketing</h2>
        <p>
            Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
        </p>
    </section>
</main>
```

- Originally the "hero image" was imported through CSS into the HTML element `<div class="hero"></div>`.
To make the web page more accessible, I added the image in the HTML document with the img element to give it semantic meaning and add the alt attribute.

```HTML
    <img alt="SEO specialists collaborating on a client project." src="./Develop/assets/images/digital-marketing-meeting.jpg" id="hero-image"/>
```

```CSS
#hero-image {
    height: 800px;
    width: 100%;
    object-fit: cover; /* Prevents the image from being distorted because there is a fixed height set. */
    margin-bottom: 25px;  
}
```

- Added alt text to the images.

- Fix the link in the navigation bar. The corresponding element was missing an `id="search-engine-optimization"`.

- I applied the BEM naming convention so the codebase is more maintainable in the long term.

- I applied my CSS resets and global settings at the top of the CSS file. I find styling and maintainibility easier with this approach.

- I consolidated as much CSS selectors as I could see possible. I had fun with this step, and played a little code golf.

- Reorganized the layout of the CSS to match the structure of the HTML file and left comments announcing the beginning of each section.

- Created custom CSS properties for the colors, again this will help ease scaling the website in the future.

```CSS
:root {
    --header-bg-color: #2a607c;
    --logo-accent-color: #d9dcd6;
    --main-content-bg-color: #0072bb; 
    --aside-content-bg-color: #2589bd;
}
```

- Next, I tested the website using the Google Chrome Screen reader, and scanned the page using the accessibility tree in the browser's developer tools. First issue I came across was the focusable elements required a more contrasting indicator to make the site more accessible. So I add the following styling:

```CSS
*:focus {
    outline: 2px solid red; /* Better contrast ratio for keyboard focusable elements */
}
```

- The Second issue I found was the file sizes for the images were far too large. This slowed the loading time of the page down significantly. I corrected the issue by reducing the file sizes in Photoshop. As the page is not image heavy. I reduced the file sizes to 250KB - 500KB max.

## Continued development

The layout is designed for desktop screen sizes only, and requires a responsive design approach so the page is optimized for any screen viewport width.

---

## Acknowledgments

[Sara Soueidan's blog on WCAG-compliant focus indicators](https://www.sarasoueidan.com/blog/focus-indicators/#new-focus-indicator-accessibility-requirements-in-wcag-2.2)

[BEM Naming Convention - getbem.com](https://getbem.com/naming/)

[Andy Bell](https://andy-bell.co.uk/a-modern-css-reset/)

[How To: Write Good Alt Text](https://supercooldesign.co.uk/blog/how-to-write-good-alt-text)

## Contributors

[Xander Rapstine](https://github.com/Xandromus)
