---
date: 2024-02-18T14:12:44+0100
title: Cats
resources:
  - src: cat-1.jpg
    title: Brown tabby cat on white stairs
    params:
      date: 2024-02-18T13:04:30+0100
  - src: cat-2.jpg
    title: Selective focus photography of orange and white cat on brown table
---
```html 
<img src="/banda.jpeg" id="target">
<script>
new Darkroom('#target', {
  // Canvas initialization size
  minWidth: 100,
  minHeight: 100,
  maxWidth: 500,
  maxHeight: 500,

  // Plugins options
  plugins: {
    crop: {
      minHeight: 50,
      minWidth: 50,
      ratio: 1
    },
    save: false // disable plugin
  },

  // Post initialization method
  initialize: function() {
    // Active crop selection
    this.plugins['crop'].requireFocus();

    // Add custom listener
    this.addEventListener('core:transformation', function() { /* ... */ });
  }
});
</script>
```
#### Social Icons

Use the `socialIcons` configuration key to add social icons on the bottom of each page:

```toml
[params]
  ...
  [params.socialIcons]
    facebook = "https://www.facebook.com/"
    instagram = "https://www.instagram.com/"
    github = "https://github.com/nicokaiser/hugo-theme-gallery/"
    youtube = "https://www.youtube.com/"
    email = "mailto:user@example.com"
    linkedin = "https://linkedin.com/"
```

