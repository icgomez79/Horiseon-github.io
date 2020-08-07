# horiseon-github.io/Code Refactor

## For the Horiseon website these are the changes that I had to make to improve the functionality and accessibility of the website:

### In HTML:
* Added the following comments between sections to facilitate the code reading.
```<!--Navigation-->,<!--Unordered list-->,<!--List elements-->,<!--Anchor elements-->,<!--Hero section-->,<!--Benefits section-->,<!--Footer-->```.
* Fixed the link for the ```<a href="#search-engine-optimization">``` changing the ```<div class="search-engine-optimization" class="search-engine-optimization">``` for ```<div id="search-engine-optimization" class="search-engine-optimization">```.
* Added the ```alt=``` values for each image in the file to ensure accesibility.

### IN CSS:
* Added the following comments between sections to facilitate the code reading.
```/*Apply styles to header*/, /* Apply styles to hero*/,/*Apply styles to benefits*/,/*Apply styles to footer*/```.
* _Consolidated this elements:_
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
    }```
**Into this**
```.benefits div {
    margin-bottom: 32px;
    color: #ffffff;
}
```
Because all had the same styles properties, I added a ```<div>``` child element to its parent ```<div class="benefits">```.
* _Erasing this css elements:_
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
 And creating only one css element 'h3', because there is only one h3 element inside the ```<div class="benefits">``` and they all have the same styles properties. Now the css code looks like this:
``` h3 {
    margin-bottom: 10px;
    text-align: center;
    }
```
* _Consolidated these elements:_
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
**To this:**
``` .benefits img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
    }
```
They all belonged to the same parent element ```<div class="benefits">``` and they have the same style properties.

* _Changed the name of these elements:_
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
**To this**
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
* _Changed these elements that have the same style properties:_
'.search-engine-optimization img {
    max-height: 200px;
    }'
'.online-reputation-management img {
    max-height: 200px;
    }'
'.social-media-marketing img {
    max-height: 200px;
    }'
**Into this**
'.content img {
    max-height: 200px;
        }'
This was posible because they all belong to the parent element ```<div class="content">``` and ```<img>```
* Finally, in order to have a better classification and easy reading of the css code I moved the '.content' css element and '.content img' to the top of the file where all the other content elements were placed.

This is an example of the old css code...
<img width="1440" alt="Screen Shot 2020-08-07 at 5 37 26 PM" src="https://user-images.githubusercontent.com/68663064/89690544-c2239680-d8d4-11ea-8c66-cb9db30fe6d4.png">

This is how it looks now...
<img width="1440" alt="Screen Shot 2020-08-07 at 5 40 15 PM" src="https://user-images.githubusercontent.com/68663064/89690700-20507980-d8d5-11ea-8f5e-eff55c63a7a5.png">


You can check the improved website in this link https://icgomez79.github.io/horiseon-github.io/

 







