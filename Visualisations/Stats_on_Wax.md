---
layout: default
title: "Stats on Wax"
show_in_menu: false
menu_order: 2
---

<style>
  /* Expand the overall site boundaries */
  .wrapper {
    max-width: 95% !important;
    margin: 20px auto !important;
    display: flex !important;
    flex-direction: row !important;
    align-items: flex-start !important;
    gap: 40px !important; /* Creates a solid buffer zone between nav and content */
  }

  /* Reset default float/width behaviors that cause overlapping */
  header {
    position: sticky !important;
    top: 20px;
    width: 220px !important; /* Locks sidebar width */
    flex-shrink: 0 !important; /* Prevents sidebar from being squished */
    margin: 0 !important;
    float: none !important;
  }

  section {
    flex-grow: 1 !important; /* Forces content block to take up all remaining right-side space */
    max-width: none !important;
    width: auto !important;
    margin: 0 !important;
    float: none !important;
    overflow-x: hidden; /* Clean edge boundaries */
  }

  /* Smooth layout fallback for smaller screens / mobile tablets */
  @media screen and (max-width: 900px) {
    .wrapper {
      flex-direction: column !important;
      gap: 20px !important;
    }
    header, section {
      width: 100% !important;
    }
  }
</style>

# Wax on Stats


<iframe width="100%" height="600" frameborder="0" src="https://observablehq.com/embed/@skankingpigeon/youtube-music-history?cell=*"></iframe>