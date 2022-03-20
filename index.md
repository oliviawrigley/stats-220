# The meme I have created:

![my_meme](https://user-images.githubusercontent.com/101959745/159187091-6e547123-ea1d-4aea-8d0b-5218aeb78e5e.png)

## The code for my meme
```r
library(magick)
#square one
before_uni <- image_read("https://media.istockphoto.com/photos/elegant-man-in-beige-suit-hat-and-eyeglasses-refusing-coffee-from-picture-id1204237201?k=20&m=1204237201&s=612x612&w=0&h=feJOnYUtbptnyJrtYhvGzbG6__RjG4hZd7wzRGne5hA=")%>% image_scale(500)

#square two
me_before <- image_blank(width = 500, height = 400, color = "#000000") %>% 
  image_annotate(text = "Me before uni", color = "#FFFFFF", size = 50,
                 font = "Impact", gravity = "center" )
#square three
at_uni <- image_read("https://media.istockphoto.com/photos/hardworking-business-man-drinks-too-much-coffee-picture-id513582516?k=20&m=513582516&s=612x612&w=0&h=5A28SC635yPgeUm609m7LCQJUiW1GGAGfxDC7Bc22IQ=") %>% image_scale(500)

#square four
me_uni <- image_blank(width = 500, height = 350, color = "#000000") %>%
  image_annotate(text = "Now, my saving grace", color = "#FFFFFF", size = 50,
                 font = "Impact", gravity = "center" )

# making the rows
top_row <- image_append(c(before_uni, me_before))
bottom_row <- image_append(c(at_uni, me_uni))

#final
c(top_row, bottom_row) %>% image_append(stack = TRUE) %>% image_scale(800)

```
### Imformation about my meme
For the meme I have created in this assignment I have taken inspiration from the following meme layouts:
* Drake Hotline Bling
* Tuxedo whinye the pooh
* Mr incredibile traumatizzato

For the content of my meme, I wanted to relate to my University experience. Before starting University, I despised coffee as I was not too fond of the taste, and I thought I could get through all my work without it. However, I was wrong; caffeine has helped pull me through. From the 8 am lectures to the all-nighters, coffee has been my saving grace. With the background of the images, the top image representing me before accepting coffee as a black background, I feel this shows me in the darkness, blind to the benefits of coffee. The second image has a white background as I think this symbols me being *'saved'* by coffee. 
