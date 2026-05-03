---
layout: default
title: Things I Make
permalink: /hobbies/
---

<style>
  /* ─── Page Shell ──────────────────────────────────────────────── */
  .hobbies-page {
    max-width: 860px;
    margin: 0 auto;
    padding: 2rem 1.25rem 5rem;
    font-family: Georgia, 'Times New Roman', serif;
    color: #1a1a1a;
  }

  /* ─── Header ──────────────────────────────────────────────────── */
  .page-header {
    border-bottom: 2px solid #1a1a1a;
    padding-bottom: 1.5rem;
    margin-bottom: 3rem;
  }
  .page-header .label {
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #888;
    margin-bottom: 0.5rem;
  }
  .page-header h1 {
    font-size: 2.8rem;
    font-weight: normal;
    line-height: 1.15;
    margin: 0 0 0.75rem;
    letter-spacing: -0.02em;
  }
  .page-header p {
    font-size: 1.05rem;
    color: #444;
    line-height: 1.7;
    max-width: 600px;
    margin: 0;
  }

  /* ─── Section Titles ──────────────────────────────────────────── */
  .section-title {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin: 3.5rem 0 1.75rem;
  }
  .section-title h2 {
    font-size: 1rem;
    font-family: 'Courier New', Courier, monospace;
    font-weight: normal;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    margin: 0;
    white-space: nowrap;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: #ccc;
  }

  /* ─── Video Grid ──────────────────────────────────────────────── */
  .video-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 1.25rem;
  }
  .video-card {
    background: #f7f5f2;
    border: 1px solid #e0ddd8;
    border-radius: 4px;
    overflow: hidden;
    transition: box-shadow 0.2s ease, transform 0.2s ease;
  }
  .video-card:hover {
    box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    transform: translateY(-2px);
  }
  .video-wrapper {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 */
    height: 0;
    overflow: hidden;
    background: #e0ddd8;
  }
  .video-wrapper iframe {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
    border: 0;
  }
  .video-caption {
    padding: 0.6rem 0.85rem 0.75rem;
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.72rem;
    color: #888;
    letter-spacing: 0.05em;
  }

  /* ─── Project Grid ────────────────────────────────────────────── */
  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 1.5rem;
  }
  .project-card {
    border: 1px solid #e0ddd8;
    border-radius: 4px;
    overflow: hidden;
    background: #fff;
  }
  .project-img {
    width: 100%;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    display: block;
    background: #f0ede8;
  }
  .project-img-placeholder {
    width: 100%;
    aspect-ratio: 4 / 3;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 0.4rem;
    background: #f0ede8;
    border-bottom: 1px solid #e0ddd8;
  }
  .project-img-placeholder .ph-icon {
    font-size: 2rem;
    opacity: 0.35;
  }
  .project-img-placeholder .ph-text {
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.65rem;
    letter-spacing: 0.1em;
    color: #aaa;
    text-transform: uppercase;
  }
  .project-body {
    padding: 0.85rem 1rem 1.1rem;
  }
  .project-body h3 {
    font-size: 1rem;
    font-weight: bold;
    margin: 0 0 0.4rem;
    letter-spacing: -0.01em;
  }
  .project-body p {
    font-size: 0.875rem;
    color: #555;
    line-height: 1.65;
    margin: 0;
  }
  .project-tag {
    display: inline-block;
    margin-top: 0.6rem;
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #999;
    border: 1px solid #ddd;
    padding: 0.15rem 0.45rem;
    border-radius: 2px;
  }

  /* ─── Blog Entries ────────────────────────────────────────────── */
  .blog-entry {
    border-top: 1px solid #e0ddd8;
    padding: 1.75rem 0;
  }
  .blog-entry:last-child {
    border-bottom: 1px solid #e0ddd8;
  }
  .blog-meta {
    display: flex;
    gap: 1rem;
    align-items: baseline;
    margin-bottom: 0.6rem;
    flex-wrap: wrap;
  }
  .blog-date {
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.7rem;
    color: #aaa;
    letter-spacing: 0.1em;
  }
  .blog-tag-topic {
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #888;
    background: #f0ede8;
    padding: 0.1rem 0.4rem;
    border-radius: 2px;
  }
  .blog-entry h3 {
    font-size: 1.2rem;
    font-weight: bold;
    margin: 0 0 0.6rem;
    letter-spacing: -0.01em;
  }
  .blog-entry p {
    font-size: 0.95rem;
    color: #444;
    line-height: 1.8;
    margin: 0 0 0.5rem;
    max-width: 640px;
  }
  .blog-readmore {
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.7rem;
    letter-spacing: 0.08em;
    color: #888;
    text-decoration: none;
    border-bottom: 1px solid #ccc;
    padding-bottom: 1px;
    transition: color 0.15s;
  }
  .blog-readmore:hover { color: #1a1a1a; border-color: #1a1a1a; }

  /* ─── Footer Note ─────────────────────────────────────────────── */
  .page-footer-note {
    margin-top: 4rem;
    padding-top: 1.5rem;
    border-top: 2px solid #1a1a1a;
    font-family: 'Courier New', Courier, monospace;
    font-size: 0.7rem;
    letter-spacing: 0.1em;
    color: #aaa;
    text-align: right;
  }

  /* ─── Responsive ──────────────────────────────────────────────── */
  @media (max-width: 520px) {
    .page-header h1 { font-size: 2rem; }
    .video-grid, .project-grid { grid-template-columns: 1fr; }
  }
</style>

<div class="hobbies-page">

  <!-- ══════════════════════════════════════════
       INTRODUCTION
       ══════════════════════════════════════════ -->
  <header class="page-header">
    <div class="label">Raied Ahmed — Personal</div>
    <h1>Things I Make</h1>
    <p>
      Outside the lab, I make things with my hands, my eyes, and whatever software happens to be open.
      This is where I collect the videos, projects, and passing thoughts that don't belong in a CV —
      but feel important anyway.
    </p>
  </header>


  <!-- ══════════════════════════════════════════
       FEATURED VIDEOS
       ══════════════════════════════════════════ -->
  <div class="section-title"><h2>Featured Videos</h2></div>

  <div class="video-grid">

    <div class="video-card">
      <div class="video-wrapper">
        <iframe
          src="https://www.youtube.com/embed/jUUbEcVFshs"
          title="YouTube video"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
      <div class="video-caption">Video 01 ·
        <a href="https://youtu.be/jUUbEcVFshs?si=q-zGBd5gb3jgzTvW" target="_blank" rel="noopener">Watch on YouTube ↗</a>
      </div>
    </div>

    <div class="video-card">
      <div class="video-wrapper">
        <iframe
          src="https://www.youtube.com/embed/HtsAU10E8yY"
          title="YouTube video"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
      <div class="video-caption">Video 02 ·
        <a href="https://www.youtube.com/watch?v=HtsAU10E8yY" target="_blank" rel="noopener">Watch on YouTube ↗</a>
      </div>
    </div>

    <div class="video-card">
      <div class="video-wrapper">
        <iframe
          src="https://www.youtube.com/embed/_GATAdcGc-w"
          title="YouTube video"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
      <div class="video-caption">Video 03 ·
        <a href="https://youtu.be/_GATAdcGc-w?si=75tJOSh5HU7G5zc_" target="_blank" rel="noopener">Watch on YouTube ↗</a>
      </div>
    </div>

    <div class="video-card">
      <div class="video-wrapper">
        <iframe
          src="https://www.youtube.com/embed/gsR-cK_6JoM"
          title="YouTube video"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
      <div class="video-caption">Video 04 ·
        <a href="https://youtu.be/gsR-cK_6JoM?si=uHKMA4fGbm8l4rAx" target="_blank" rel="noopener">Watch on YouTube ↗</a>
      </div>
    </div>

    <div class="video-card">
      <div class="video-wrapper">
        <iframe
          src="https://www.youtube.com/embed/DLTZMhSLBBU"
          title="YouTube video"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
      <div class="video-caption">Video 05 ·
        <a href="https://youtu.be/DLTZMhSLBBU?si=-6hE6H9iAuI6F3m_" target="_blank" rel="noopener">Watch on YouTube ↗</a>
      </div>
    </div>

    <div class="video-card">
      <div class="video-wrapper">
        <iframe
          src="https://www.youtube.com/embed/utSZn2ahLc0"
          title="YouTube video"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
      <div class="video-caption">Video 06 ·
        <a href="https://www.youtube.com/watch?v=utSZn2ahLc0" target="_blank" rel="noopener">Watch on YouTube ↗</a>
      </div>
    </div>

  </div><!-- /video-grid -->


  <!-- ══════════════════════════════════════════
       HOBBY PROJECTS
       ══════════════════════════════════════════ -->
  <div class="section-title"><h2>Hobby Projects</h2></div>

  <div class="project-grid">

    <!-- Project 1: MS Paint Paintings -->
    <div class="project-card">
      <!--
        TO ADD YOUR OWN IMAGE:
        Replace the placeholder block below with:
        <img src="/assets/images/mspaint-collection.jpg" alt="MS Paint paintings" class="project-img">
      -->
      <div class="project-img-placeholder">
        <span class="ph-icon">🖼️</span>
        <span class="ph-text">Add image here</span>
      </div>
      <div class="project-body">
        <h3>MS Paint Gallery</h3>
        <p>
          A growing collection of paintings made entirely in Microsoft Paint.
          No layers, no undo history — just the humble fill bucket and a steady mouse hand.
        </p>
        <span class="project-tag">Digital Art</span>
      </div>
    </div>

    <!-- Project 2: Crocheted Sweater -->
    <div class="project-card">
      <!--
        TO ADD YOUR OWN IMAGE:
        Replace the placeholder block below with:
        <img src="/assets/images/crochet-sweater.jpg" alt="Crocheted sweater" class="project-img">
      -->
      <div class="project-img-placeholder">
        <span class="ph-icon">🧶</span>
        <span class="ph-text">Add image here</span>
      </div>
      <div class="project-body">
        <h3>Crocheted Sweater</h3>
        <p>
          My first full garment — a sweater crocheted from scratch.
          Picking the yarn, counting the stitches, frogging entire rows:
          slower than expected, and more satisfying than anything else I've made.
        </p>
        <span class="project-tag">Crochet</span>
      </div>
    </div>

    <!-- Project 3: Sewn Bag -->
    <div class="project-card">
      <!--
        TO ADD YOUR OWN IMAGE:
        Replace the placeholder block below with:
        <img src="/assets/images/sewn-bag.jpg" alt="Handmade sewn bag" class="project-img">
      -->
      <div class="project-img-placeholder">
        <span class="ph-icon">🧵</span>
        <span class="ph-text">Add image here</span>
      </div>
      <div class="project-body">
        <h3>Handmade Bag</h3>
        <p>
          Cut and sewn from scratch — no pattern, just a rough sketch and a lot of seam-ripping.
          The kind of thing that makes you appreciate every bag you've ever owned.
        </p>
        <span class="project-tag">Sewing</span>
      </div>
    </div>

  </div><!-- /project-grid -->

  <!--
    ┌─────────────────────────────────────────────────────────┐
    │  HOW TO ADD MORE PROJECTS                               │
    │                                                         │
    │  Copy a .project-card block above and:                  │
    │  1. Swap the placeholder div for an <img> tag           │
    │  2. Update the <h3> title                               │
    │  3. Update the <p> description                          │
    │  4. Update the .project-tag label                       │
    └─────────────────────────────────────────────────────────┘
  -->


  <!-- ══════════════════════════════════════════
       THOUGHTS & BLOG
       ══════════════════════════════════════════ -->
  <div class="section-title"><h2>Thoughts & Blog</h2></div>

  <!-- ── Entry (Placeholder) ─────────────────── -->
  <div class="blog-entry">
    <div class="blog-meta">
      <span class="blog-date">2025 · Month DD</span>
      <span class="blog-tag-topic">Crochet</span>
    </div>
    <h3>On learning slowly</h3>
    <p>
      I started the sweater thinking it would take two weeks. It took closer to two months.
      Somewhere in the middle I stopped minding — the repetition of each stitch started to
      feel less like delay and more like the whole point. There's something worth paying
      attention to in work that can't be sped up.
    </p>
    <p>
      I'm not sure yet whether that feeling transfers to other things. But I've been thinking
      about it while I work.
    </p>
    <!-- Optional: link to a longer post
    <a href="/posts/on-learning-slowly" class="blog-readmore">Continue reading →</a>
    -->
  </div>

  <!--
    ┌─────────────────────────────────────────────────────────┐
    │  HOW TO ADD A NEW BLOG ENTRY                            │
    │                                                         │
    │  Copy the .blog-entry block above and update:           │
    │  - .blog-date  → your post date (e.g. "2025 · Jun 10") │
    │  - .blog-tag-topic → topic label (e.g. "Painting")     │
    │  - <h3>  → your entry title                             │
    │  - <p>   → your entry text (add as many <p> as needed)  │
    │                                                         │
    │  Entries stack top-to-bottom; newest at the top.        │
    └─────────────────────────────────────────────────────────┘
  -->


  <!-- ══════════════════════════════════════════
       FOOTER NOTE
       ══════════════════════════════════════════ -->
  <div class="page-footer-note">
    ← <a href="/">Back to main page</a> &nbsp;·&nbsp; Updated whenever something new gets made.
  </div>

</div><!-- /hobbies-page -->
