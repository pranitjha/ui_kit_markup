# Hero Component

## Current Markup

```
<div class="coh-container ssa-component coh-component ssa-component-instance-1f9a5df0-3f7f-4f2f-82ab-ee186e8f5290 coh-component-instance-1f9a5df0-3f7f-4f2f-82ab-ee186e8f5290 image-no-overlay ssa-instance-b57b5db90d53fc0d75a567f7576fbcb8 coh-ce-cpt_hero-453a75b5">
  <nav class="coh-container semi-transparent-dark-background coh-ce-cpt_hero-fedf769c" aria-label="Breadcrumb">
    <ul class="coh-breadcrumb coh-style-breadcrumbs">
      <li>  <a href="/">Home</a>  </li>
       <li>  <a href="/node"></a>  </li>
    </ul>
  </nav>
  <div class="coh-container tall center-align-content coh-style-padding-top-bottom-large coh-ce-cpt_hero-48d68960 coh-container-boxed">
    <div class="coh-container text-content coh-ce-cpt_hero-77bc8a97">
      <h1 class="coh-heading heading coh-style-text-color-dark-background coh-ce-cpt_hero-fd5ded85"> Hero Component </h1>
      <div class="coh-wysiwyg coh-style-text-color-dark-background">
        <p>This is Hero component.</p>
      </div>
      <a href="#" class="coh-link coh-style-link-button-color coh-ce-cpt_hero-55f19225" target="_self"> Find out more    </a>  
    </div>
    <div class="coh-container drop-zone-content coh-ce-cpt_hero-65b810ab">     </div>
  </div>
</div>
```

### Issues with current Markup
* Empty div present if there are no `dropzone` items.
* Empty breadcrumbs links for current page.
* Missing `aria-current` attribute for the current page.

## Suggested Markup

```
<div class="coh-container ssa-component coh-component ssa-component-instance-1f9a5df0-3f7f-4f2f-82ab-ee186e8f5290 coh-component-instance-1f9a5df0-3f7f-4f2f-82ab-ee186e8f5290 image-no-overlay ssa-instance-b57b5db90d53fc0d75a567f7576fbcb8 coh-ce-cpt_hero-453a75b5">
  <nav class="coh-container semi-transparent-dark-background coh-ce-cpt_hero-fedf769c" aria-label="Breadcrumb">
    <ul class="coh-breadcrumb coh-style-breadcrumbs">
      <li>  <a href="/">Home</a></li>
       <li>  <a href="/node" aria-current="page">Page title</a></li>
    </ul>
  </nav>
  <div class="coh-container tall center-align-content coh-style-padding-top-bottom-large coh-ce-cpt_hero-48d68960 coh-container-boxed">
    <div class="coh-container text-content coh-ce-cpt_hero-77bc8a97">
      <h1 class="coh-heading heading coh-style-text-color-dark-background coh-ce-cpt_hero-fd5ded85"> Hero Component </h1>
      <div class="coh-wysiwyg coh-style-text-color-dark-background">
        <p>This is Hero component.</p>
      </div>
      <a href="#" class="coh-link coh-style-link-button-color coh-ce-cpt_hero-55f19225" target="_self"> Find out more    </a>  
    </div>

    <!--The below div should be removed if there are no component dropzone items -->
    <div class="coh-container drop-zone-content coh-ce-cpt_hero-65b810ab"></div>

  </div>
</div>
```