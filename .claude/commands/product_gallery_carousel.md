# Rewrite the product media gallery to make it a slideshow
product-media-gallery.liquid is used in product detail page to show the product images. Currently on desktop the image viewer (line 59 - 127) is controlled by a list of thumbnails (line 179 - 331) below. There are no previous or next buttons to show the previous or next image. We want to make it a slideshow on desktop as well.

On mobile, however, you can swipe to previous or next image.

Follow the instructions below and think step by step. Propose the code changes. Output your code change in .claude/output/product-slideshow.diff. Do not write anycode yet. Ultrathink.

# Instructions
1. Read the product-media-gallery and media-gallery.js to understand how it works.
2. Use what we are already doing on mobile to add the previous and next buttons to the image viewer on desktop only.