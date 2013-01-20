# Assignment One: HTML/CSS
This is a multi-part assignment with the objective of making you comfortable working with HTML and CSS. In completing this assignment, you will have styled the HTML of a standard, but complex, website home page, and created a website of your own.

**Note:** Only CSS and HTML need to be used for this assignment. If you're using JavaScript (or libraries such as jQuery), you might be thinking a little too hard about how to do this.

**Note 2:** If you've never had a CS account before, one has been set up for you (provided you were enrolled in the class through Banner as of last night). You should visit the Sunlab (CIT 143) and talk to the consultant on duty (the student sitting at the first computer when you walk in) about setting up your account. TAs are also available to help you through this process.

**Note 3:** If this assignment seems overwhelming to you, please come see a TA on hours to talk through some strategies for tackling it. This assignment has been designed so that it is feasible for both concentrators and non-concentrators to complete in a reasonable amount of time.

### Important questions to consider before starting:
* What is the "Box Model"?
* What is a CSS Selector? What is the difference between id and class attributes?
* What does the CSS `position:fixed` do?
* What are image sprites? (Know how to move sprites with attributes `background-position`).
* What are CSS pseudo-classes?
    For link tags `<a>` (i.e., `a:hover`, `a:active`, `a:visited`) as well as generally (with `:lastchild`).
* What's the difference between `display:inline`, `display:block`, `display:inline-block`?

## Part Zero
In this class, all of your assignments will be based around web technologies. To facilitate your work, we provide you with web space inside of the CS department that you can use (henceforth referred to as the assignments server). If any of these instructions look intimidating to you, please come to hours so a TA can help you with the setup process.

The assignments server is a shared hosting environment running PHP. It is only accessible from within the CS department. Each student is assigned their own directory which is accessible via the department filesystem (`/web/cs132/<username>`) and via a subdomain (`http://<username>.proj132.cs.brown.edu`).

Before beginning work on the first assignment, you'll have to set up your account on the assignments server. To do so, run `cs132_web_init` from the command line. That command does the following things:

1. Creates a symlink from `~/course/cs132/www` to `/web/cs132/<username>`. If you don't know what this means, don't worry about it; all it means is that you can `cd` using either path to get to your web directory.
2. Prompts you to create a password (henceforth known as your "website password"), which it then uses to password protect your site from the web. Keep this password secret and do not share it with anyone! Doing so is a violation of the Collaboration Policy.
3. Sets up environment variables (`db_host`, etc) so your scripts can use them to connect to the database. We will cover this part in more detail later in the class.

Once that's done, you should be able to access `http://<username>.proj132.cs.brown.edu` using your CS username and website password. If the website doesn't load at all, you're probably on the wrong network -- the assignments server will only work from inside the department. (For more information on accessing the department network remotely, check out [Portable Sunlab][psunlab].)

  [psunlab]: http://www.cs.brown.edu/about/system/net_remote/portable_sunlab/

## Part One
#### Getting Started
* Run the command `cs132_install html`. This creates the files you will need for this assignment. They can be found in `/web/cs132/<username>/html`.
* All images needed for this assignment are given to you in the images folder
* **Do not edit** `appstack.html` at any point in this assignment
* `style_base.css` is the linked CSS file for `appstack.html`
    * It is located in the `css/` folder.
* **Only edit** `style_base.css` for this assignment.

#### Specifications
* Using CSS, style `appstack.html` to look like the image mockups provided. *And make sure to click through to see it in full size*.

    [![Appstack Mockup](HTML_part1_mockup.png)](HTML_part1_mockup.png)
* The navigation bar should stay at the top of the screen when scrolling.
    * Note: see [facebook.com](http://facebook.com) or [techcrunch.com](http://techcrunch.com)
* All image links should have hover actions. See the annotated image mock-up (*and make sure to click through to see it in full size*).

    [![Annotated Appstack Mockup](HTML_part1_annotated.png)](HTML_part1_annotated.png)
* The main container on the page should be centered in the browser window.
* Hint: As you might notice in looking through the stencil code, the navigation bar buttons are an image sprite. To make your life easier, we've calculated certain attributes for the sprites that you might find useful:
    * "Unhovered" buttons: `background-position, y value: 0;`
    * "Hover" buttons: `background-position, y value: -59px;`
    * Features Button: `width: 90px; background-position, x value: 0;`
    * Pricing Button: `width: 80px; background-position, x value: -91px;`
    * Addons Button: `width: 90px; background-position, x value: -172px;`
    * About Button: `width: 72px; background-position, x value: -263px;`
    * Customers Button: `width: 105px; background-position, x value: -437px;`
    * Blog Button: `width: 65px; background-position, x value: -543px;`

Note: While we don't require pixel perfect accuracy in this assignment, your styled webpage must be consistent on all major browsers (Chrome and Firefox). To access the latest versions of each browser available in the department, follow these instructions:

* Firefox: From the command-line, type 'firefox_stable'. Note that Iceweasel, the department's default browser, is not an acceptable substitute.
* Chrome: From the command-line, type 'google-chrome'.

## Part Two
There are 2 options: You can either create your own personal web page, or create a new CS132 course website.

#### Getting Started
You're on your own for this one. Use Part 1 and the resources provided on the course website for references in your work. **Hint: Do Part 1 before you do Part 2**.

#### Option 1: Personal Website
##### Specifications
1. Your website needs a home page.
2. 3-5 linked pages.
3. A navigation bar that connects the pages.

Note: your hand-in should be comparable in complexity to the current CS132 course website.

#### Option 2: New CS132 Course Website
##### Specifications
1. A clearly displayed title image/logo that includes the text "CS132: Creating Modern Web Applications".
2. Separate pages for News, Staff, Assignments, Resources, and Projects containing the current data. The current course website has all the information you should include.
3. A navigation bar which links to News, Staff, Assignments, Resources, and Projects pages.

## Handing In
When you have completed the assignment, you should `cd` into your `html` directory and type `cs132_handin html`. This will hand in all of your code to the TAs.
