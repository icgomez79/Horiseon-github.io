# horiseon-github.io/Code Refactor

## For the Horiseon website these are the changes that I had to make to improve the functionality and accessibility of the website:

### In HTML:
* Added the following comments between sections to facilitate the code reading.
```<!--Navigation-->,<!--Unordered list-->,<!--List elements-->,<!--Anchor elements-->,<!--Hero section-->,<!--Benefits section-->,<!--Footer-->```.
* Added the tags ```<header></header>```
* Fixed the link for the ```<a href="#search-engine-optimization">``` changing the ```<div class="search-engine-optimization" class="search-engine-optimization">``` for ```<div id="search-engine-optimization" class="search-engine-optimization">```.
* Added the ```alt=``` values for each image in the file to ensure accesibility.

#### This is how it looks the html file now...

<img width="1440" alt="Screen Shot 2020-08-07 at 6 50 58 PM" src="https://user-images.githubusercontent.com/68663064/89694878-12542600-d8e0-11ea-9dc3-2142986f452f.png">

### IN CSS:
* Added the following comments between sections to facilitate the code reading.
```/*Apply styles to header*/, /* Apply styles to hero*/,/*Apply styles to benefits*/,/*Apply styles to footer*/```.
* **Consolidated this elements:**
```.benefit-lead {
    margin-bottom: 32px;
    color: #ffffff;
    }
    .benefit-brand {
    margin-bottom: 32px;
    color: #ffffff;
    }
    .benefit-cost {
    margin-bottom: 32px;
    color: #ffffff;
    }
```
**For this**
```.benefits div {
    margin-bottom: 32px;
    color: #ffffff;
}
```
Because all had the same styles properties, I added a ```<div>``` child element to its parent ```<div class="benefits">```.
* **Erasing this css elements:**
``` .benefit-lead h3 {
    margin-bottom: 10px;
    text-align: center;
    }
    .benefit-brand h3 {
    margin-bottom: 10px;
    text-align: center;
    }
    '.benefit-cost h3 {
    margin-bottom: 10px;
    text-align: center;
    }
```
 And because there is only one h3 element inside the ```<div class="benefits">``` and they all have the same styles properties, now the css code looks like this:
``` h3 {
    margin-bottom: 10px;
    text-align: center;
    }
```
* **Consolidated these elements:**
```.benefit-lead img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
    }
    .benefit-brand img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
    }
    .benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
    }
```
**For this:**
``` .benefits img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
    }
```
They all belonged to the same parent element ```<div class="benefits">``` and they have the same style properties.

* **Changed the name of these elements:**
``` .search-engine-optimization {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
    }
    .online-reputation-management {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
    }
    .social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
    }
```
**For this**
``` .content div {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}
```
They all belong to the same parent element ```<div class="content">``` and inside a '<div>' element, so I was able to consolidated them in one css element. 
* **Changed these elements that have the same style properties:**
```.search-engine-optimization img {
    max-height: 200px;
    }'
'.online-reputation-management img {
    max-height: 200px;
    }'
'.social-media-marketing img {
    max-height: 200px;
    }
```
**For this**
```.content img {
    max-height: 200px;
        }
```
This was posible because they all belong to the parent element ```<div class="content">``` and ```<img>```
* Finally, in order to have a better classification and easy reading of the css code I moved the ```.content``` css element and ```.content img``` to the top of the file where all the other content elements were placed.

#### This is an example of the previous css code...

<img width="1440" alt="Screen Shot 2020-08-07 at 6 58 06 PM" src="https://user-images.githubusercontent.com/68663064/89694949-521b0d80-d8e0-11ea-892c-605d1b71a90f.png">

#### This is how it looks now...

<img width="1440" alt="Screen Shot 2020-08-07 at 6 53 53 PM" src="https://user-images.githubusercontent.com/68663064/89694935-3fa0d400-d8e0-11ea-8d9a-d0c216ec9be5.png">


You can check the improved website in this link https://icgomez79.github.io/horiseon-github.io/

© 2020 Horiseon. All rights reserved. 
 







