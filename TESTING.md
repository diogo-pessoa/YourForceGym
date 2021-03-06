## Testing

### Code Validation

#### HTML validator
- [W3C HTML Validator](https://validator.w3.org/)

| File | Validator check  | screenshot| 
|---|---|---|
| index.html | ok | [home](https://github.com/diogo-pessoa/YourForceGym/blob/master/readme-files/testing/validator/home_validator.png)|
| gallery.html | ok | [gallery](https://github.com/diogo-pessoa/YourForceGym/blob/master/readme-files/testing/validator/gallery_validator.png)|
| contact.html |  ok | [contact](https://github.com/diogo-pessoa/YourForceGym/blob/master/readme-files/testing/validator/contact_validator.png)|
| about.html | ok | [about](https://github.com/diogo-pessoa/YourForceGym/blob/master/readme-files/testing/validator/about_validator.png)|


#### CSS validator

- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/validator)
   
|File| Validator check|
|---|---|
| style.css | ok |

---

### Responsiveness

| Device | Screen Size  | Home  | Gallery |  Contact | About |
|---|---|---|---|---|---|
| Iphone5 | 320px/568px | ok | ok | ok | ok |
| Iphone6 | 375px/667px | ok | ok | ok | ok | ok |
| Ipad | 768px/1024px | ok | ok |  ok | ok | ok |
| PC | >960px | ok |  ok | ok | ok | ok |

### Browsers

| Browser | Home | Gallery | Contact-Us | About |
|---|---|---|---|---|
| Firefox | ok  | ok | ok | ok | 
| Chrome  | ok |ok | ok | ok | 

---
### Manual tests per User Story

1. Social Media Footer Links 
   
   1.1 As a User I want external links to open on a new tab. 

   1.2 **Test** From every page on project, navigate to footer and click on every social network anchor icon. Make sure all open right path in a new tab.

2. Refactoring Header Section
    
    2.1 As a Developer I want a cleaner header section on pages, having a aligned navbar 
    
    2.2 Simplify grid Structure
    
    2.3 reduce amount of space used by header
    
    2.4 *Test* visit Page on different screen sizes confirm navigation is natural and responsive, no elements break
  
3. Sticky NavBar to ScreenTop onscroll.
    
    3.1 *Test* navigate to all pages Scroll down confirm expected behaviour

4. About Page 
 
    4.1 As a website owner, I want  Share with the user information about Gym, the classes available and Trainers details.

    4.2 Test page is responsive on all tested screen sizes
    
    4.3 NavBar sticks to top of page when scroll down happens

    4.4  About Gym 
    
    4.5 Body font-size was too small

    4.6 Fix return to default size. 
    
    4.7 Classes Section
       - I want to know which classes are available in the gym, With access to a time table.
       - timetable PDF button on about page
       - clicking on `check timetable` button open pdf on new tab
       - Improving Element Spacing with better padding
       - h5 element wasn't responsive on smaller resolutions

    4.8 Improve responsiviness on **Meet our trainers** section 
       - make sure trainer Bio fills space well when opening page on different screen sizes
       - Image stays proportional to screen sizes and responds to change in resolution.  
    
5. Gallery

    5.1 Refactoring page structure to improve responsiviness
        - Improving spacing between sections
        - reviewing grid system to keep headings aligned


6. Merging Contact and find-us page

    6.1 **Testing** during manual testing it made sense to merge these pages together, as neither are heavy in content.
    
    6.2 Split contact page in two sections, adding the `Find Us` at the bottom with an `id='find-us'`. By leveraging the ID I can set the links to redirect the user straight to this Section.

7. Links Test

  7.1 - Menu links
         
|Link| index | gallery | Contact | About |opens in New_tab|
|---|---|---|---|---|---|
| Home | ok | ok |ok |ok |no|
| Gallery | ok | ok |ok |ok |no|
| Find Us | ok | ok |ok |ok |no|
| Contact | ok | ok |ok |ok |no|
| About | ok | ok |ok |ok |no|

  7.2   Footer links
|Link| index | gallery | Contact | About |opens in New_tab|
|---|---|---|---|---|---|
| Find Us | ok | ok |ok |ok |no|
| Facebook | ok | ok |ok |ok |yes|
| Twitter | ok | ok |ok |ok |yes|
| Instagram | ok | ok |ok |ok |yes|


7.3 Contact.html form links

|Link| Contact | opens in New_tab|
|---|---|---|
| About Us | ok |no|
| trainers| ok |no|
| Free Classes| ok |no|
| Gym amenities | ok |no|
| here | ok |no|


8. Sticky nav to page top 

    8.1 **User story** As a developer I want to have the menu available on top of the page for ease of navigation. 

    8.2 **Test** during tested Some pages would show bug on of jumping screen on the scroll down event. 

    8.3 Added a div to wrap navbar and keep page structure the same on scroll down. 

    8.4 Manual test by visiting each page and scrolling down on different browsers and resolutions.

    Firefox
    ---

    | Device | Screen Size  | Home  | Gallery |  Contact | About | 
    |---|---|---|---|---|---|
    | Iphone5 | 320px/568px | ok | ok | ok | ok |
    | Iphone6 | 375px/667px | ok | ok | ok | ok | ok |
    | Ipad | 768px/1024px | ok | ok |  ok | ok | ok |
    | PC | >960px | ok |  ok | ok | ok | ok |
    ---
    Chrome
    ---

    | Device | Screen Size  | Home  | Gallery |  Contact | About | 
    |---|---|---|---|---|---|
    | Iphone5 | 320px/568px | ok | ok | ok | ok |
    | Iphone6 | 375px/667px | ok | ok | ok | ok | ok |
    | Ipad | 768px/1024px | ok | ok |  ok | ok | ok |
    | PC | >960px | ok |  ok | ok | ok | ok |
        

### Bug-fixes

1. At Iphone5 The header of the page is cut-off on width.
   1.1 **Fix** changed the Col structure on the Header section to better organize Headings and improve responsiviness.
 
2. `find-us` link redirects to Visit-us page. 
    
    2.1 bug found anchor has no href destination;
    
    2.2 **Test** Navigate to each page in Site click `Find us` in footer. Confirmed find-us link open correct path and doesn't pop user for a new tab.
  
    2.3 **Fix**: update the href attribute from element with proper `findus.html` path. Removed `target="_blank"` from anchor element.

3. Reducing brigthness on yellow on site.
    
    3.1 As a developer I want a tone of yellow that keeps a good contrast with black, but is not to bright.
    
    3.2 *Test* navigate to each page and review `buttons` and `NavBar` all have respect the color scheme.

4. *Discovered while testing* on (iphone5/6) contact.html page doesn't scroll properly. 
    
    4.1 **Fix**:  adding `class=content` to section in body

5. *Found while testing* while hovering on `h1` Your Force Gym, animation is blue, using browser default.
    
    5.1 **Fix**: add `hvr-grow` class to element.

6. Pixalated carousel images on large screens:
    
    6.1 As a user, I want the quality of the image to be the same from mobile to larger screen.
    
    6.2 **Test** The images on the carousel don't have a high enough resolution and appear pixelated on Larger screens
    
    6.3 **Fix** replaced images with higher resolution on large screens 

7. for about page h5 on classes section was overflowing the width of the screen. 
    
    7.1 **Test** open about page in differen screen-sizes 
        
    7.2 **Fix** Refactoring of the classes section removing the h5 element from class `col` and improving responsiviness

8. Header Section heading elements overlowing on Iphone 5 responsiveness check

    8.1 **Fix** reviewed content and elements, adjust to fit well on all screen sizes

9. Gallery
    
    9.1 Discovered while testing

    9.2 re-used image from carousel was updated, causing one of the gallery images to go missing

