---
description: Through photography, the beauty of Mother Nature can be frozen in time. This category celebrates the magic of our planet and beyond — from the immensity of the great outdoors, to miraculous moments in your own backyard.
featured_image: azzedine-rouichi-ZS_XuDZmxpM-unsplash.jpg
menus: "main"
sort_by: Name # Exif.Date
sort_order: desc
title: Nature
#type: gallery
weight: 3
params:
  theme: dark
---
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

