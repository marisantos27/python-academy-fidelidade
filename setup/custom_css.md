# Custom Reveal CSS

## How to Update the CSS Files to Format your Reveal Slides

NBConvert uses templates depending on the type of conversion you want to achieve. More information [here](https://nbconvert.readthedocs.io/en/latest/customizing.html#selecting-a-template).

### Change Print Color

By default, my print messages were returning with black color font on top of a black backgroun, which was impossible to read.
The goal is to convert the font color used in the `<pre>` tags by chaning the CSS configurations.

1. Go to the templates directory, get the 'reveal' configuration and change the `custom_reveal.css` file.
The full list of available paths can be found in `$ jupyter --paths`

*/home/francisco/anaconda3/share/jupyter/nbconvert/templates/reveal/static/custom_reveal.css*

2. Add a new configuration for font-color in the `.reveal pre {}` block

```css
.reveal pre {
  color: #FFFFFF;
  /*{OTHER THINGS}*/
```
