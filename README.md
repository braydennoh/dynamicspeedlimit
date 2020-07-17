# Dynamic Speed Limit System Project
### Brayden Noh, Ben Davis, John Stanwick

![voltage and current pwm cah-2](https://user-images.githubusercontent.com/67966231/87812799-5e063900-c826-11ea-81d8-7fae5194df47.jpg)

The objective was to create a speed limit system based on surrounding weather conditions. 

The system can sense rain intensity and fog visibility. Values obtained are used as calculation inputs. 

v = [-2 + √(4+2* s / 9.8 * f )] * (9.8 * f ) 

In the equation, v is recommended vehicle speed, s is driver visibility, and f is road surface friction. The equation has been previously established by finding driver reaction and available braking distance and time. 

# Visibility Distance

Fog affects the vehicle stopping distance. With images, there are several differences between a picture with and without fogs. Contrast, saturation, and brightness are distinct, however, not correlating. For an accurate algorithm, a dark channel feature was used, which uses non-sky dark pixels on an image, usually found in borderlines and shadows.

J dark (x) = 〖min┬(y∈Ω(x) ) (〗⁡min┬cÒ{r,g,b} ⁡〖J^c 〗  (y))	

Below, the figure shows the distance estimation with the dark channel feature. 

<img width="984" alt="Capture" src="https://user-images.githubusercontent.com/67966231/87812593-0f589f00-c826-11ea-820c-242922b97fb6.PNG">

# Road Surface Friction

There are two main factors determining the road friction: rain and temperature. A rain gauage was used to determine the rain intensity and a temperature sensor for the other factor. We needed a method for combining these two factors. Hartman Model was used as our solution. This model  predicts road friction by having a example dataset. For example, if I know the friction value during rain rate of 0.15 mm.h and 30


- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)


For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/braydennoh/dynamicspeedlimit/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
