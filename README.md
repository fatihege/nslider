![NSlider Logo](https://imgupload.io/images/2021/06/28/nslider.png)

---

# NSlider
NSlider is a lightweight (< 10 KB), modern and customizable JavaScript slider library.

---

## CDN

> Development
> > https://cdn.jsdelivr.net/gh/fatihege/nslider@1.0.0/src/js/nslider.js
> 
> > https://cdn.jsdelivr.net/gh/fatihege/nslider@1.0.0/src/css/nslider.css

> Production
> > https://cdn.jsdelivr.net/gh/fatihege/nslider@1.0.0/src/js/nslider.min.js
> 
> > https://cdn.jsdelivr.net/gh/fatihege/nslider@1.0.0/src/css/nslider.min.css


---

## Sample Usage
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>NSlider</title>
    <link rel="stylesheet" href="nslider.min.css">
    <!-- Custom styling for slider to look neat. -->
    <style>
        .nslider {
            width: 500px;
            height: 200px;
            background-color: #e2e2e2;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="nslider">
        <div class="nslider-wrapper">
            <div class="nslider-slide" id="slide-1">
                Slide 1
            </div>
            <div class="nslider-slide" id="slide-2">
                Slide 2
            </div>
            <div class="nslider-slide" id="slide-3">
                Slide 3
            </div>
        </div>
        <div class="nslider-button nslider-button-prev"></div>
        <div class="nslider-button nslider-button-next"></div>
    </div>
</div>
<script src="nslider.min.js"></script>
<script>
    const slider = new NSlider({ // Only 'elem' key required.
        elem: document.querySelector('.container'), // A parent element of the slider
        // NOTE: The specified parent element can have only 1 NSlider.
        
        // animation: true, // Animation opens with default settings
        
        animation: { // Custom Animation Options
             duration: 1000, // Milliseconds
             timingFunction: 'ease-in' // CSS's animation timing functions
        },
        
        keyboardControl: true, // Slider can be controlled with right and left arrows
        // currentSlide: 2, // Current slide index. It starts from 0 because it is in array logic
        // prevButtonInner: '<', // Custom "previous" button content
        // nextButtonInner: '>', // Custom "next" button content
        dots: true, // Dots as the number of slides below the slider
    });
    
    // Optional
    setInterval(() => slider.next(), 5000); // Every 5 seconds the slider automatically moves to the next slide
    // setInterval(() => slider.prev(), 5000); // Every 5 seconds the slider automatically moves to the previous slide
</script>
</body>
</html>
```

The result of this example:

![Example Result](https://imgupload.io/images/2021/06/28/image97cdc48ac9b970ee.png)
