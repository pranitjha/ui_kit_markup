# Tabs container horizontal/vertical & tab item component

## current Markup

```
<div class="coh-accordion-tabs-inner coh-accordion-tabs-display-tabs-xl coh-accordion-tabs-display-accordion-ps coh-style-accordion-tabs-keyline-dark-text coh-accordion-tabs-horizontal-left coh-ce-cpt_tabs_container_horizontal_ta-c16ec5fd coh-accordion-tabs-display-tabs" data-once="cohAccordionTabs">
  <ul class="coh-accordion-tabs-nav">
    <li class="">
      <a href="#4257225834-1341054554" data-once="loadEvent">Enter label here</a>
    </li>
    <li class="is-active">
      <a href="#4257225834-86704003" data-once="loadEvent">Enter label here</a>
    </li>
  </ul>
  <div class="coh-accordion-tabs-content-wrapper">
    <div class="coh-accordion-title" data-coh-tab-settings="[]" data-once="tab-init">
      <a href="#4257225834-1341054554" data-once="loadEvent" aria-expanded="false">Enter label here</a>
    </div>
    <div id="4257225834-1341054554" class="coh-accordion-tabs-content ssa-component coh-component ssa-component-instance-202f900e-a891-43bd-8cc6-d8dc16f11cd0 coh-component-instance-202f900e-a891-43bd-8cc6-d8dc16f11cd0" style="display: none;">
      <div class="coh-container coh-style-padding-small ssa-instance-42cc3e6911b4cdb23f67ffc1e018d297 coh-ce-cpt_tab_item-1177bf71">
        <img class="coh-image ssa-component coh-component ssa-component-instance-20056b3e-53ee-4564-9124-90fc93d6b0b8 coh-component-instance-20056b3e-53ee-4564-9124-90fc93d6b0b8 coh-style-margin-bottom-small coh-ce-cpt_image-2cc57305 coh-image-responsive-xl coh-lazy-loaded" loading="lazy" data-src="/sites/default/files/styles/coh_medium_landscape/public/images/default-images/Image-placeholder.png?itok=BO95B9CQ" alt="" data-once="lazyload-once" src="/sites/default/files/styles/coh_medium_landscape/public/images/default-images/Image-placeholder.png?itok=BO95B9CQ" data-was-processed="true">
      </div>
    </div>
    <div class="coh-accordion-title is-active" data-coh-tab-settings="[]" data-once="tab-init">
      <a href="#4257225834-86704003" data-once="loadEvent" aria-expanded="true" aria-disabled="true">Enter label here</a>
    </div>
    <div id="4257225834-86704003" class="coh-accordion-tabs-content ssa-component coh-component ssa-component-instance-e35ce088-5c56-4949-a2ef-9dcf44546b64 coh-component-instance-e35ce088-5c56-4949-a2ef-9dcf44546b64 is-active" style="display: block;">
      <div class="coh-container coh-style-padding-small ssa-instance-fb8f52c51036f378cfccb5621c20c9c3 coh-ce-cpt_tab_item-1177bf71">
        <div class="coh-wysiwyg ssa-component coh-component ssa-component-instance-dae255c7-c79b-492d-8016-ef817f10e131 coh-component-instance-dae255c7-c79b-492d-8016-ef817f10e131  coh-style-text-color-light-background        ssa-instance-402c9eff8f51905205898e231f2523df coh-ce-cpt_text-fa10298a">
          <p>This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on. This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on. This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on. This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on.</p>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Issues with current markup

* For better accessibility, we can use `role="tablist"` and `role="tab"` for the tab list and tab items respectively.
* Adding `role="tabpanel"` to the tab content will help screen readers to understand that the content is a tab panel.
* We can add `aria-selected="true"` to the active tab item and `aria-selected="false"` to the inactive tab items. When the tab is selected, we can set `aria-selected="true"` and `aria-selected="false"` to the previously selected tab item.


## Suggested markup

```
<div class="coh-accordion-tabs-inner coh-accordion-tabs-display-tabs-xl coh-accordion-tabs-display-accordion-ps coh-style-accordion-tabs-keyline-dark-text coh-accordion-tabs-horizontal-left coh-ce-cpt_tabs_container_horizontal_ta-c16ec5fd coh-accordion-tabs-display-tabs" data-once="cohAccordionTabs">
  <ul class="coh-accordion-tabs-nav" role="tablist">
    <li class="">
      <a href="#4257225834-1341054554" data-once="loadEvent" role="tab" aria-selected="false">Enter label here</a>
    </li>
    <li class="is-active">
      <a href="#4257225834-86704003" data-once="loadEvent" role="tab" aria-selected="true">Enter label here</a>
    </li>
  </ul>
  <div class="coh-accordion-tabs-content-wrapper">
    <div class="coh-accordion-title" data-coh-tab-settings="[]" data-once="tab-init">
      <a href="#4257225834-1341054554" data-once="loadEvent" aria-expanded="false" role="tab" aria-selected="false">Enter label here</a>
    </div>
    <div id="4257225834-1341054554" class="coh-accordion-tabs-content ssa-component coh-component ssa-component-instance-202f900e-a891-43bd-8cc6-d8dc16f11cd0 coh-component-instance-202f900e-a891-43bd-8cc6-d8dc16f11cd0" style="display: none;" role="tabpanel">
      <div class="coh-container coh-style-padding-small ssa-instance-42cc3e6911b4cdb23f67ffc1e018d297 coh-ce-cpt_tab_item-1177bf71">
        <img class="coh-image ssa-component coh-component ssa-component-instance-20056b3e-53ee-4564-9124-90fc93d6b0b8 coh-component-instance-20056b3e-53ee-4564-9124-90fc93d6b0b8 coh-style-margin-bottom-small coh-ce-cpt_image-2cc57305 coh-image-responsive-xl coh-lazy-loaded" loading="lazy" data-src="/sites/default/files/styles/coh_medium_landscape/public/images/default-images/Image-placeholder.png?itok=BO95B9CQ" alt="" data-once="lazyload-once" src="/sites/default/files/styles/coh_medium_landscape/public/images/default-images/Image-placeholder.png?itok=BO95B9CQ" data-was-processed="true">
      </div>
    </div>
    <div class="coh-accordion-title is-active" data-coh-tab-settings="[]" data-once="tab-init">
      <a href="#4257225834-86704003" data-once="loadEvent" aria-expanded="true" aria-disabled="true" role="tab" aria-selected="true">Enter label here</a>
    </div>
    <div id="4257225834-86704003" class="coh-accordion-tabs-content ssa-component coh-component ssa-component-instance-e35ce088-5c56-4949-a2ef-9dcf44546b64 coh-component-instance-e35ce088-5c56-4949-a2ef-9dcf44546b64 is-active" style="display: block;" role="tabpanel">
      <div class="coh-container coh-style-padding-small ssa-instance-fb8f52c51036f378cfccb5621c20c9c3 coh-ce-cpt_tab_item-1177bf71">
        <div class="coh-wysiwyg ssa-component coh-component ssa-component-instance-dae255c7-c79b-492d-8016-ef817f10e131 coh-component-instance-dae255c7-c79b-492d-8016-ef817f10e131  coh-style-text-color-light-background        ssa-instance-402c9eff8f51905205898e231f2523df coh-ce-cpt_text-fa10298a">
          <p>This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on. This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on. This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on. This is placeholder text. If you are reading this, it is here by mistake and we would appreciate it if you could email us with a link to the page you found it on.</p>
        </div>
      </div>
    </div>
  </div>
</div>

```
