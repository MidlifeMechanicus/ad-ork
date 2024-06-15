# Website refresh

This was a surprisingly challenging project. Intended as a simple website refresh, it turned out that the host uses Spanglefish 2, and interface from 2012 that allows only limited access to raw html and css.

As such, I had to scrap my original flex-box design, and work first on creating a structure that duplicated the immutables of the Spanglefish 2 framework.

Some creative use of DevTools allowed me to find the necessary ID information to change some aspects of the platform that were not available to the public normally. However, to avoid tampering Spanglefish 2 seems to use near-maximum specificity in the background css, making it very difficult to alter or override any of the framework parameters. Ultimately, any such change is a great deal of effort for very little gain.

While I have made notes in the various files about what can be changed and what cannot, some things that stand out:

* Flex-box does not work.
* The bottom banner can only take an image, not text. I got around this in the short term by mounting text on an image.
* Spanglefish 2 cannot import new fonts.
* Spanglefish 2 does not accept @media queries. Instead, it automatically tries to reformat the website when it detects a mobile viewer. A lot of things break when it does that.
* Following on from the above, post-launch it was discovered that unordered lists do not get resized in mobile view, while ordered lists do. This meant quickly changing all unordered lists to ordered lists; the end result is viewable, but not ideal stylistically.