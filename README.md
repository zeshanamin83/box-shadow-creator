# What is Box Shadow Creator?

Get perfect shadows every time for the no-designer this is perfect for a quick box shadow solution.

# Installation

`npm i box-shadow-creator`

## Basic usage for JavaScript

```
function boxShadowCreator(options) {
    let images = document.querySelectorAll('.box-shadow');

    if (options.shadow_type === 'hard') {
        options.shadow_type = '0px';
    } else { 
        options.shadow_type = '15px';
    }

    images.forEach(image => {
        image.style.boxShadow = `10px 10px ${options.shadow_type} 1px rgba(0,0,0,0.12)`;

        if (options.padding) {
            image.style.padding = '1em';
        }
    }) 
}
```

## Basic usage for npm users

```
import { boxShadowCreator } from 'box-shadow-creator';

boxShadowCreator({
    shadow_type: 'soft',
    padding: false
})
```

## All Options

Box shadow creator supports 2 options, both of which are optional:
* *shadow_type* - _hard / soft_ (defaults to soft)
* *padding* - _boolean_ (defaults to false)
