# Modal window component

## current Markup

```
<div class="coh-modal">
   <div class="coh-modal-overlay" data-modal-close-btn="" style=""></div>
   <div class="coh-modal-inner modal-medium js-first-focus is-open" data-modal-document="" tabindex="0" style="" role="document">
      <div class="coh-container content-wrapper coh-ce-cpt_modal_window-50d5c6fb">
         <!-- modal content -->
      </div>
      <div class="coh-modal-close-wrapper"> <button aria-label="Close" class="coh-modal-close-button coh-style-modal-close-button-color js-last-focus" data-autofocus="" data-modal-close-btn=""></button></div>
   </div>
</div>
```

### Issues with current markup

* It's always a good practice to add the `type="button"` attribute to buttons.

## Suggested markup

```
<div class="coh-modal">
   <div class="coh-modal-overlay" data-modal-close-btn="" style=""></div>
   <div class="coh-modal-inner modal-medium js-first-focus is-open" data-modal-document="" tabindex="0" style="" role="document">
      <div class="coh-container content-wrapper coh-ce-cpt_modal_window-50d5c6fb">
         <!-- modal content -->
      </div>
      <div class="coh-modal-close-wrapper"> <button aria-label="Close" class="coh-modal-close-button coh-style-modal-close-button-color js-last-focus" data-autofocus="" data-modal-close-btn="" type="button"></button></div>
   </div>
</div>

```
