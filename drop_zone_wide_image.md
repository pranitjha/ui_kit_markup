# Drop zone and wide image component

## current Markup

```
<div class="coh-container ssa-component coh-component ssa-component-instance-3871fd9b-c2f8-4372-8771-2c358d0cc741 coh-component-instance-3871fd9b-c2f8-4372-8771-2c358d0cc741 ">
   <div class="coh-container ssa-instance-42b858d057cfed9132913161f32d617b coh-ce-cpt_drop_zone_and_wide_image-a17bdac8">
      <div class="coh-container coh-container-boxed">
         <div class="coh-row coh-row-bleed-xl coh-row-visible-xl" data-coh-row-match-heights="[]" data-once="coh-row-match-heights-init">
            <div class="coh-row-inner   coh-ce-cpt_drop_zone_and_wide_image-40886e00">
               <div class="coh-column coh-ce-cpt_drop_zone_and_wide_image-2265c5c coh-visible-sm coh-col-sm-12 coh-visible-lg coh-col-lg-5 coh-visible-xl coh-col-xl-5">
                  <div class="coh-container coh-style-padding-top-bottom-large coh-ce-cpt_drop_zone_and_wide_image-bf5611cb coh-container-boxed">     </div>
               </div>
               <div class="coh-column image-column coh-ce-cpt_drop_zone_and_wide_image-399455a4 coh-visible-sm coh-col-sm-12 coh-visible-xl coh-col-xl-6">
                  <div class="coh-container image-object-fit-cover coh-ce-cpt_drop_zone_and_wide_image-232e84bb"> <img class="coh-image coh-image-responsive-xl" src="/sites/default/files/styles/coh_large/public/images/default-images/Background-placeholder.png?itok=a9280eOv" alt="Placeholder"> </div>
               </div>
            </div>
         </div>
      </div>
   </div>
</div>
```

### Issues with current markup

* Unneccessary div container
* We can use margin to add the white space on top and bottom instead of padding and then remove the additional div container to reduce the markup.

## Suggested markup

```
<div class="outer-container with-margins">
   <div class="inner-boxed-container">
      <div class="row">
         <div class="inner-row">
            <div class="col>
               <div class="container-for-dropzone">
               
               </div>
            </div>
            <div class="col>
               <div class="container-for-image">
                  <img src="" alt="" />
               </div>
            </div>
         </div>
      </div>
   </div>
</div>

```
