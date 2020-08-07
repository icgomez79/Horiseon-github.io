# horiseon-github.io Code Refactor

##For the Horiseon website these are the changes that I had to make to improve the functionality and accesibility:

In HTML:
Added comments between sections to facilitate the code reading.
Fixed the link for the search-engine-optimization changing the "div class "for "div id".
Added the "alt" values for each image in the file to ensure accesibility.

IN CSS:
Added comments between sections to facilitate the code reading.
Consolidated the "benefit-lead", "benefit-brand" and "benefit-cost" elements styles in one (because all had the same styles applied) adding a div element child to its parent "benefits".
Erasing ".benefit" from "benefit-lead h3", "benefit-brand h3", "benefit-cost h3", because is the only h3 inside benefits, and it was redundant. Also I consolidated them in one because the have the same styles applied.
Changing "benefit-lead img", "benefit-brand img" and benefit-cost img to "benefits img", due they belong to the same parent element class and it was necessary to add each class to de ccs code. Also, because they have the same style properties I consolidated them in one element class.
Changed the elements "search-engine-optimization","online-reputation-management" and "social-media-marketing" for ".content" because they all belong to the same parent element class "content" and going this I consolidated them in one style element.
Changed the elements "search-engine-optimization img","online-reputation-management img" and "social-media-marketing img" for ".content img" because they all belong to the same parent element class "content img" and going this I consolidated them in one style element.
Moved the ".content" and ".content img" to the top of the file where all the other content elements were placed, in order to have a better classification.

 







