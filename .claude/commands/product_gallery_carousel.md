# Rewrite the product media gallery to make it a slideshow
product-media-gallery.liquid is used in product detail page to show the product images. Currently on desktop the image viewer (line 59 - 127) is controlled by a list of thumbnails (line 179 - 331) below. There are no previous or next buttons to show the previous or next image. We want to make it a slideshow on desktop as well.

On mobile, however, you can swipe to previous or next image.

Refer to the Guildline below but explore all the potential issue that you may have. Propose your code change and output your code change in .claude/output/product-slideshow.diff. Do not write anycode yet. Ultrathink step by step.

# Guildline
1. Read the product-media-gallery, media-gallery.js, and global.js (line 727 - 1065) to understand how it works. Trace down the code step by step to see how the thumbnail click event is handled and how the active thumbnail is set.
2. You will need to attached a listener on the image viewer's previous and next button, and you may need to add a new function in global.js or media-gallery.js to handle the click event.
3. Remove the previous and next buttons from the thumbnails on desktop.
4. Make sure the active thumbnail is always visible when you click on the previous or next button.