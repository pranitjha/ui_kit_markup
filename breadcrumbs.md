# Breadcrumbs component

## current Markup

```
<nav class="coh-container aria-label="Breadcrumb">
   <ul class="coh-breadcrumb coh-style-breadcrumbs">
      <li><a href="/">Home</a></li>
   </ul>
</nav>
```

### Issues with current markup

* As per ARIA standards, breadcrumbs should be inside an ordered list instead of unordered list.
* The above markup was taken from an internal page. As you can see, the breadcrumbs does not include the current page. Breadcrumbs should always include the 
   current page link as the last list item.
* The last link must have the aria attribute - `aria-current=page` to indicate the screen readers about the current page the user is in.

## Suggested markup

```
<nav class="coh-container aria-label="Breadcrumb">
   <ol class="coh-breadcrumb coh-style-breadcrumbs">
      <li><a href="/">Home</a></li>
      <li><a href="/internal" aria-current="page">Internal page</a></li>
   </ol>
</nav>

```
