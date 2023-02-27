# Site footer component

## current Markup

```
<footer class="coh-container ssa-component coh-component ssa-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f coh-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f coh-style-footer-light-theme menu-position-desktop--center coh-style-focusable-content coh-ce-cpt_site_footer-a55124d3">
   <div class="coh-container primary-row coh-ce-cpt_site_footer-7db95991">
      <div class="coh-container coh-ce-cpt_site_footer-607d5298"> </div>
      <div class="coh-container">
         <nav class="coh-container footer-menu coh-ce-cpt_site_footer-1a90bda">
            <ul class="coh-menu-list-container coh-unordered-list coh-ce-c2e6bd89">
               <li class="coh-menu-list-item coh-ce-c2a716e9 js-coh-menu-item" data-coh-settings="{&quot;xl&quot;:&quot;hidden&quot;}" data-once="js-coh-menu-item-init"></li>
            </ul>
         </nav>
      </div>
      <div class="coh-container coh-ce-cpt_site_footer-6c573274">
         <ul class="coh-list-container coh-unordered-list ssa-component coh-component ssa-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f coh-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f social-links coh-ce-cpt_social_links-c4355378">
            <li class="coh-list-item coh-ce-cpt_social_links-ff917e8c1 coh-ce-cpt_social_links-ff917e8c"> <a href="https://www.facebook.com/acquia" class="coh-link facebook coh-ce-cpt_social_links-7fba61701 coh-ce-cpt_social_links-7fba6170" target="_blank" aria-label="Follow us on Facebook" rel="noopener"> </a> </li>
         </ul>
      </div>
   </div>
   <div class="coh-container secondary-row coh-ce-cpt_site_footer-6b4ab1ad">
      <div class="coh-container coh-ce-cpt_site_footer-595b4965">
         <div class="coh-wysiwyg">
            <p>53 State street, 10th Floor, Boston, MA 02109, 888-922-7842</p>
         </div>
      </div>
      <div class="coh-container coh-ce-cpt_site_footer-7974db9e">
         <div class="coh-wysiwyg">
            <p>Copyright&nbsp;© 2020 Acquia, Inc. All Rights Reserved.</p>
         </div>
      </div>
   </div>
</footer>
```

### Issues with current markup

* If there are no nav links, the markup is still outputting an empty nav element

## Suggested markup

```
<footer class="coh-container ssa-component coh-component ssa-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f coh-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f coh-style-footer-light-theme menu-position-desktop--center coh-style-focusable-content coh-ce-cpt_site_footer-a55124d3">
   <div class="coh-container primary-row coh-ce-cpt_site_footer-7db95991">
      <div class="coh-container coh-ce-cpt_site_footer-607d5298"> </div>
      <div class="coh-container">
      </div>
      <div class="coh-container coh-ce-cpt_site_footer-6c573274">
         <ul class="coh-list-container coh-unordered-list ssa-component coh-component ssa-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f coh-component-instance-a0525d85-a8d2-4188-8381-fceef6f4a32f social-links coh-ce-cpt_social_links-c4355378">
            <li class="coh-list-item coh-ce-cpt_social_links-ff917e8c1 coh-ce-cpt_social_links-ff917e8c"> <a href="https://www.facebook.com/acquia" class="coh-link facebook coh-ce-cpt_social_links-7fba61701 coh-ce-cpt_social_links-7fba6170" target="_blank" aria-label="Follow us on Facebook" rel="noopener"> </a> </li>
         </ul>
      </div>
   </div>
   <div class="coh-container secondary-row coh-ce-cpt_site_footer-6b4ab1ad">
      <div class="coh-container coh-ce-cpt_site_footer-595b4965">
         <div class="coh-wysiwyg">
            <p>53 State street, 10th Floor, Boston, MA 02109, 888-922-7842</p>
         </div>
      </div>
      <div class="coh-container coh-ce-cpt_site_footer-7974db9e">
         <div class="coh-wysiwyg">
            <p>Copyright&nbsp;© 2020 Acquia, Inc. All Rights Reserved.</p>
         </div>
      </div>
   </div>
</footer>

```
