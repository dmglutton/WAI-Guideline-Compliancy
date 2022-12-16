# Refactoring HTML to Add Accessibility 

## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:| 
| HTML    | [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) | 
| CSS     | [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)      |   
| Git | [https://git-scm.com/](https://git-scm.com/)     |    

## Description 

[Visit the Deployed Site]( https://joshmatsumoto.github.io/Code-Refactor-Site/)

This project refactors code to be more accessible through: semantic HTML tags; descriptive text as an alternative for images; a user interface that adjusts for differant screen sizes; and removing code that may be seen as redundant or distracting. The end goal of the project was to, at a minimum, allow for a pleasurable experience if the end user was using an e-reader.



## Code Refactor Example

What are the steps required to install your project? Provide a step-by-step description of how to get the development environment running.


```html
<div class="header">
        <h1>Hori<span class="seo">seo</span>n</h1>
        <div>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </div>
    </div>
```

Converting the above non-semantic div with the class of 'header' to an appropriate [<header> semantic element](https://www.w3schools.com/html/html5_semantic_elements.asp). 

```html
<header>
        <h1>Hori<span class="seo">seo</span>n</h1>
        <nav>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </nav>
    </header>

```

This change require some additional modification to the CSS selector: 

```css
.header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
}
```

No longer targeting the element on the page with the class of 'header' but instead the css selector targeting the 'header' element 

```css
header {
    display: flex;
    padding: 45px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
    justify-content:space-between
}

```
Added a media screen element to add a navigation menu window at smaller viewport sizes

```css
@media screen and (max-width: 1020px) {
    header nav{
        display:flex;
        flex-direction:column;
        height:300px
    }
    header nav ul{
        flex-direction:column;
        background-color: #2a607c;

    }
    header nav ul li{
        height:50px;
    }
}

## Usage 

n/a

```md

```


## Learning Points 

It was really fun to apply some of the skills I have learned so far like
HTML semantics and using the flexbox and media query to adjust content within the viewport


## Author Info

```md

* [Portfolio](n/a "yet ;))
* [LinkedIn](https://www.linkedin.com/in/joshua-matsumoto-7629ab259/)
* [Github](https://github.com/joshmatsumoto)
```

