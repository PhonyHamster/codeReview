# One-minute Introduction

`difr` is a light-weighted, free and non-restricted tools for code review.

`difr` accepts a diff file as input and converts it into an HTML file with an embedded editor for adding comments.

Users can edit the comments, save the comment files, or copy the page to their emails. 

### Installation

1. Download Java 
2. Download a jar [here](https://www.dropbox.com/s/sbqgcseosbqwdzc/difr.jar).

### Sample output

![Sample output](http://nxt.flotsam.nl/difr.png)

### Typical use cases

To create a review page for the diff between your working copy and what's currently on HEAD:

    git diff | java -jar difr.jar > /tmp/review.html

To create a review page for your feature branch, if you're using git flow:

    git flow feature diff {feature} | java -jar difr.jar > /tmp/review.html
    
Or if that's too much trouble, pass the HTML produced directly to your browser, using [bcat](http://rtomayko.github.io/bcat/), which is what I do all the time:

    git flow feature diff {feature} | java -jar difr.jar | bcat

To get help on the options `difr` accepts, type:

    java -jar difr.jar -h



