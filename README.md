# My Perosnal Webpage

## Webpage Design Documentation

### 1. Webpage Building Intent

The core intention of building this personal website is to promote myself to prospective employers. 
The website would contain 5 main sections. These sections are “About Myself”, “Experience”, “Portfolio”, “Future” and “Contact”. 

It is critical to allow interested audience to view my personal webpage on their mobile gadgets. Therefore, the website layout is 
designed around mobile first philosophy. Moreover, it is important to create a webpage that is functional on browsers such as Safari, 
Chrome, Firefox and Internet Explorer because targeted audience may have different browser installed on their mobile gadgets. 

---

### 2. Webpage Building Approach

At the start, I had considered three different approaches building my webpage. The first approach is by using free and ready available 
themes from popular websites / blogs. The second approach is to start from scratch by writing completely new HTML 5 and CSS 3 files. 
The third approach is to use popular frameworks such as Bootstrap or Zurb Foundation.  All these approaches have its advantages and disadvantages.

| Approaches       | Advantages                                                          | Disadvantage                                                                                           |
| :--- |:---|:---|
| **Free Themes**  | - Desktop / mobile layout is setup properly                         | - Need to understand how the theme is built before adding or modifying features / effects              |
|				   | - Browser compatibility coverage is broad	                         | - Limited flexibility                                                                                  |
|				   | - Modify existing contents easily			                         |                                                                                                        |
| **From Scratch** | - Great flexibility on generating contents / features / effects     | - More time and effort needed to layout responsiveness for both desktop and mobile screens             |
|                  | - Maintain all contents easily                                      | - All areas of browser compatibility need to be tested                                                 |
| **Framework**    | - Tested and reliable                                               | - The files generated for the project may be larger overall due to additional custom css and js files  |
|                  | - Enable developer to focus more on producing contents              |                                                                                                        |
|                  | - Use ready available JS plugin embedded within the framework to add in special features / effects |                                                                         |

**Table 1** : Personal opinion on different approaches for building website

Eventually, I had decided to use Bootstrap 3.3.7 framework to build my personal webpage. The short duration permitted and the mobile first 
requirements for this project are the reasons that influence my final decision. By using this framework, it allows me to concentrate on generating
contents that are responsive. Secondly, it would allow some valuable time to research and implement better mobile user experience features. 

---

### 3. Webpage Design Approach

Before starting any codes on HTML and CSS file, I had opted to perform some wireframe exercises. This exercise had saved me extra time since the 
wireframe outcome instantly gives me an idea how my website would look like in both desktop and mobile screens. After this exercise, I created a 
personal logo based on my first name. 

#### 3.1 Style Guide

During the wireframe process, I had chosen to limit the number of colours used for the webpage because I only wanted to promote my contents but 
not my front-end UX/UI skills. In fact, I had tested out a few sets of different colours combination. In the end, I had only used dark blue (#0B1625), 
yellow (#ECE833), white (#FFF) and grey (#808080) colours. As for the font, I only used a single Google font-style across the webpage. The font-family 
chosen is Lato and the fallbacks are "Helvetica Neue", Helvetica and Arial. The font size and weight are adjusted accordingly to suit various screen 
sizes display. Paddings between text and paragraphs are also applied where necessary. Please refer below for the wireframe exercise accomplished.

#### 3.2 Personal Logo and Navigation Bar

The personal logo is located on the left hand side of the fixed navigation bar. This logo position is similar to where a business logo or a brand 
would normally be located.  The links for each main section of the webpage would be floated towards the right hand side of the navigation bar. All
the links would be clearly shown at breakpoint width more than or equal to 768px. The section links would be consolidated into a burger style button
at breakpoints width less than 768px.  

 
#### 3.3 Carousel Container and About Myself Section

The subsequent container is a Bootstrap carousel container that contains three different images and its respective image caption. This container
is not declared as a main section but a brief opening section at the start once the page is loaded. “About Myself” section would be the following
container right after the carousel container. The container contains an underlined heading and three paragraphs. 


#### 3.4 Background Image Container & Experience Section & Portfolio Section
The next container would be used to store images and a “read more” button. The “Experience” section is followed on with an underlined heading
and three paragraphs as well. Subsequent container is for containing “Portfolio” section. This section has a total of three separate individual 
heading, three toggle buttons, three separate individual sub-heading, three separate individual paragraphs and three separate individual images.

#### 3.5 Future Section & Contact Section & Footer Section
The second last section is the “Future”. It has a total of two individual blocks of containers. The first container has a heading, four paragraphs 
and a logo slider. The second container has an underlined main heading. This is followed by three separate images and thumbnails at the bottom of 
each image. The final section is the “Contact”. The container contains an underlined heading and two paragraph, a form input field, a send button 
and three different social icons. A footer section is included which has all the main section links and a back to top arrow link.

---

### 4. Bootstrap 3.3.7 Responsive Framework & Other Plugins
As mentioned earlier, Bootstrap 3.3.7 framework is used to build this webpage. Hence, most of the container responsiveness is handled by the 
in-built CSS classes for various screen sizes (i.e. col-lg-x / col-md-x / col-sm-x / col-xs-x) where x is ranging from 1 to 12. These values are
specified in different container tags to suit both desktop and mobile wireframes design layout. However, there are few elements that do not rely
on Bootstrap responsive theme. The main reason is due to the addition of non bootstrap feature/effects implemented into the webpage. All the 
features/effects added in are to enhance user browsing and navigating experience.

#### 4.1 Navigation Bar
The navigation section is fixed at the top of the page using class navbar-fixed-top. This also means that the navigation bar will always appear at 
the top of the screen wherever the user scrolls downward. In order to save some screen estate, I had included a headroom.js plugin combined with 
some jquery script to hide the navigation bar as the user scroll downward to other contents. The navigation bar will be shown as the user scroll upward. 
This headroom.js plugin is hosted by WickyNilliams on Github. The jquery script can be referred inside the HTML body tag under “<!-- For Hiding and Showing Navbar onScroll -->”.

The burger toggle button will also slide in a menu bar from the left when is clicked. This menu slide in feature is a non standard Bootstrap feature and is 
implemented using Bootstrap-Offcanvas plugin contributed by Phil Hughes on Github. The reason for this implementation is to adopt current mobile menu design trend.


#### 4.2 Carousel Container
In the carousel container section, Bootstrap carousel.js is used. In fact, left (i.e. previous) and right (i.e. next) controls has been left out. 
This action was taken because of two main reasons. The first is not to allow these controls to further impede the view of the images in mobile layout. 
Secondly, the carousel indicators would be sufficient for the user to cycle through the carousel. TouchSwipe j.query plugin hosted by Matt Bryson on Github 
is included onto the carousel container. This plugin allows user to swipe through the carousel images. Additional JavaScript would be needed and can be referred
at script outside the HTML body tag “//For Carousel Swipe Touch Function (Refering to Jquery Mobile Touch-gesture JavaScript)”. In reality, this is a standard 
feature on mobile gadgets if carousel images are to be added. 

Special effects have also been added to the first image of the carousel and the image captions. These effects are implemented using Animate.css plugin 
hosted by Daniel Eden on Github combined with some JavaScript written by Maria Antonietta Perna at Sitepoint. User can notice that once the page is loaded, 
the first carousel image will zoom in from out. This is accomplished by JavaScript found inside the HTML body tag under “<!-- For Carousel Image ONLY animation -->”.
The image caption will slide upward from the bottom instantaneously at every cycled image. This effect is to spice up the caption appearance. 
Final effect in this section is the caption would fade away gradually as the user scroll down using simple JavaScript. This effect is worthwhile because it
actually inform the user that he/she is leaving the current container and should be focusing the contents on the upcoming container. Please refer to script outside
the HTML body tag “//Fade Carousel Caption when Schroll down” for details.

When the screen resizes, the carousel images also resize. This responsive feature on the image is needed since Bootstrap carousel default is override by other
CSS properties.  Please refer to script outside the HTML body tag “//For Responsive Carousel Images when screen resizes” for details.

#### 4.3 About Myself Section
In “About Myself” section, the container (i.e. #about-wrapper) have higher index value than the carousel container (i.e. #carousel-img). 
This setup is to enable parallax effect over the carousel images. The real purpose of including a parallax effect is to create an illusion of depth 
in a 2D scene and adding to the immersion. This effect would not work if JavaScript is not added. Please refer to script inside the HTML body tag 
“<!-- For Parallax Effect over Carousel -->” for details. The contents within the container would slide in from the left as user scroll towards the viewport. 
As the user leaves the viewport, the contents would disappear. This is the combination of JavaScript and CSS written by Simon Codrington at Sitepoint. 
The benefit of this is to provide an interesting and interactive experience to engage the user. Please refer to script inside the HTML body tag “<!--For About Myself Contents -->”
for details.

#### 4.4 Background Image Container
In this container (#"experience-sec0), parallax effect over the background images has been implemented. The script details can be found script inside the HTML
body tag under “<!-- For Parallax -->”. This effect is added not only create an illusion similar to “About Myself” section but also encourage user to view more 
of the image when scrolling upward and downward. Unfortunately, this plugin does not work on Android and IOS devices. The image would static without any degradation. 
A hover effect has been introduced to the “read more” button although hover does not really work well on mobile gadgets. However, the user would still be able to appreciate 
the effect because the CSS pseudo-class :focus is applied with same attributes. This means that if user clicked on the button the effect could still be seen. 

#### 4.5 Experience Section
Contents within this container (i.e. #experience-sec) would slide up from the bottom as user scroll towards the viewport. As the user leaves the viewport, the contents 
would disappear. This is the combination of JavaScript and CSS written by Simon Codrington at Sitepoint. Please refer to script inside the HTML body tag “<!-- For Experience Contents -->” 
for details.

#### 4.6 Portfolio Section
In this container (i.e. # portfolio-sec) would slide in from the left as user scroll towards the viewport. As the user leaves the viewport, the contents would disappear. 
This is the combination of JavaScript and CSS written by Simon Codrington at Sitepoint. Please refer to script inside the HTML body tag “<!-- For Portfolio Contents -->” for details.

Once the user is in the viewport, user could toggle on so called “button” labelled as 1, 2 and 3 to show different portfolios. It is important to note that the first portfolio 
under “button 1” is always shown once user is in the viewport.  The user can click on button 2 and button 3 to review other portfolios. Each portfolio would slide¬ in from the 
bottom once user clicked on the button 2 and button 3. Again, this is the combination of JavaScript and CSS written by Simon Codrington at Sitepoint. Please refer to script 
outside the HTML body tag “<!-- Portfolio Section -->” for details. The reason for this implementation is to allow more user interaction with my contents and help reduce the user’s 
scrolling footprint.

#### 4.7 Future Section
The contents of this container (i.e. # future-project-sec) have two noticeable features. The first one is having a slider container that cycle through all the logos infinitely.
This feature is implemented by using a minified JavaScript file and some scripts within the HTML body tag together with other CSS. The details can be found on 
“<!-- For Skills Logo/Icon Slider -->”. The advantage of having this slider is that it could save some space within the container and giving these logo a tidy inline look.

#### 4.8 The second feature can be seen on ‘Future Project’ section. The three different projects would bounce in from different angles as user scroll towards the 
viewport. As the user leaves the viewport, the contents would disappear. This is the combination of JavaScript and CSS written by Simon Codrington at Sitepoint. 
Please refer to script inside the HTML body tag “<!-- Future Project Section -->” for details. It is a good feature inclusion when user is anticipating your future projects.

#### 4.9 Contact Section
This section is straightforward. All responsiveness used Bootstrap CSS theme. Formspree.io is used for email and message input fields. This tool offers 1000 
submissions per email each month and it is sufficient for static webpage. The social links are included using font-awesome icons with some special CSS pseudo 
class :hover and :focus effect.

#### 4.10 Footer Section
This section does not any special features apart from giving each specified section links and the back to top arrow a smooth scrolling effect. 
This is achieved by including a script outside of the HTML body tag which can be found under “<!-- Script for Individual Section Scroll -->” for individual section 
and “<!--Script for Scroll to Top from footer Section -->” for the back to top button.

#### 4.11 Additional Feature
User may also notice that a floating back to top button would appear on the screen when viewport is 200mm from the top of the screen. This script is 
implemented on the outside of the HTML body tag under “<!-- Section of Scroll to Top Visible/Invisible Button -->”.

---

### 5. HTML & CSS Files

##### HTML File

The HTML file is written in accordance with HTML 5 standards using English as the HTML language.  <! DOCTYPE html> is specified at the 
very beginning so that web browsers can read the HTML file. Within the <head> tag, several important meta tags are included. These are written as followed; 

* <meta charset="utf-8">
* <meta http-equiv="X-UA-Compatible" content="IE=edge">
* <meta name="viewport" content="width=device-width, initial-scale=1">

Other meta tags such as <meta name="description" content=" "> and <meta name="author" content=" "> are supplementary. These tags if included, allow web browser 
search engines to capture all information and display below the webpage link of the HTML file. Social media meta tags are included as well. These are written as followed;

* <meta property="og:title" content=" ">
* <meta property="og:description" content=" ">
* <meta property="og:type" content=" ">
* <meta property="og:image" content=' ‘>

The rest of the HTML file is followed by a <body> tag that keeps all the HTML contents. 


