# Slide container & slide item component

## current Markup

```
  <div class="coh-slider-container" id="main-slider-1" role="region">
    <div class="coh-slider-nav-top"></div> 
    <div class="coh-slider-container-mid">
      <div class="coh-slider-container-inner slick-initialized slick-slider">
        <div class="coh-slider-nav-inner-top">
          <button type="button" class="slick-prev coh-style-slider-navigation-left slick-arrow" style="" aria-label="Previous slide"></button>
          <button type="button" class="slick-next coh-style-slider-navigation-right slick-arrow" style="" aria-label="First slide"></button>
        </div>
        <div class="slick-list draggable">
          <div class="slick-track" style="opacity: 1; width: 6552px; transform: translate3d(-2016px, 0px, 0px);">
            <div class="coh-slider-item slick-slide slick-cloned" role="group" data-slick-index="-1" aria-label="slide 1" id="" aria-hidden="true" tabindex="-1" style="width: 504px;">
              <img class="coh-image coh-image-responsive-xl coh-lazy-loading" loading="lazy" alt="Placeholder" data-once="lazyload-once" src="Image-placeholder.png?itok=FKiac4ZO" data-was-processed="true">
            </div>
            <div class="coh-slider-item slick-slide slick-cloned" role="group" data-slick-index="11" aria-label="slide 2" id="" aria-hidden="true" tabindex="-1" style="width: 504px;">
             <img class="coh-image coh-image-responsive-xl coh-lazy-loading" loading="lazy" alt="Placeholder" data-once="lazyload-once" src="Image-placeholder.png?itok=FKiac4ZO" data-was-processed="true">
            </div>
          </div>
        </div>
        <div class="coh-slider-nav-inner-bottom"></div>
      </div>
    </div>
    <div class="coh-slider-nav-bottom"></div>
  </div>
```

### Issues with current markup

* The `coh-slider-nav-top` and `coh-slider-nav-bottom` can be removed depending on the navigation style.
* The `coh-slider-nav-inner-top` and `coh-slider-nav-inner-bottom` can be removed depending on the navigation style.

* As per ARIA standards, the `role="region"` should be used only when the content is not a landmark region. In this case, the slider is a landmark region and hence the `role="region"` is not required.
* `aria-roledescription="carousel"` should be added to the main slider container to indicate the screen readers that the content is a carousel.
* It's a good practice to add `arai-live="polite"` to the main slider container to indicate the screen readers that the content is updated dynamically using prev and next buttons. This will help the screen readers to announce the changes to the users. If the slider is not updated dynamically, then `aria-live="off"` should be added to the main slider container.



## Suggested markup

```
  <div class="coh-slider-container" id="main-slider-1" aria-live="polite/off" aria-roledescription="carousel">
    <div class="coh-slider-nav-top"></div> <!-- we can keep either this or the bottom div depeneding on the requirement -->
    <div class="coh-slider-container-mid">
      <div class="coh-slider-container-inner slick-initialized slick-slider">
        <div class="coh-slider-nav-inner-top">
          <button type="button" class="slick-prev coh-style-slider-navigation-left slick-arrow" style="" aria-label="Previous slide"></button>
          <button type="button" class="slick-next coh-style-slider-navigation-right slick-arrow" style="" aria-label="Next slide"></button>
        </div>
        <div class="slick-list draggable">
          <div class="slick-track" style="opacity: 1; width: 6552px; transform: translate3d(-2016px, 0px, 0px);">
            <div class="coh-slider-item slick-slide slick-cloned" role="group" data-slick-index="-1" aria-label="slide 1" id="" aria-hidden="true" tabindex="-1" style="width: 504px;">
              <img class="coh-image coh-image-responsive-xl coh-lazy-loading" loading="lazy" alt="Placeholder" data-once="lazyload-once" src="Image-placeholder.png?itok=FKiac4ZO" data-was-processed="true">
            </div>
            <div class="coh-slider-item slick-slide slick-cloned" role="group" data-slick-index="11" aria-label="slide 2" id="" aria-hidden="true" tabindex="-1" style="width: 504px;">
             <img class="coh-image coh-image-responsive-xl coh-lazy-loading" loading="lazy" alt="Placeholder" data-once="lazyload-once" src="Image-placeholder.png?itok=FKiac4ZO" data-was-processed="true">
            </div>
          </div>
        </div>
        <div class="coh-slider-nav-inner-bottom"></div> <!-- we can keep either this or the top div depeneding on the requirement -->
      </div>
    </div>
    <div class="coh-slider-nav-bottom"></div> <!-- we can keep either this or the top div depeneding on the requirement -->
  </div>

```
