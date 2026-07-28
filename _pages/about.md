---
layout: about
title: about
permalink: /
subtitle: Augustine Louvrier

images:
  slider: true

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p><a href="mailto:augustinelouvrier@gmail.com">augustinelouvrier@gmail.com</a></p>
    <p><a href="https://www.linkedin.com/in/augustinelouvrier" target="_blank">LinkedIn</a></p>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I'm Augustine, an MChem student at Imperial College London, going into my third year. I am most interested in the areas of cosmetics, skincare and fragrance.

In this blog I want to write about anything that piques my interest in this field. I want to push my limits of chemical understanding by exploring actual research papers and trying to digest the information in the form of a blog. I also want to create some articles where I break down chemistry topics into simpler terms for anyone to learn from.

Besides chemistry, I enjoy drawing and painting, cooking, and sailing. I am the incoming vice commodore of the Imperial College Sailing Club. 

<div style="clear: both;"></div>

<style>
  .carousel-label {
    text-align: center;
    font-weight: 600;
    margin: 2.25rem 0 0.6rem;
  }
  .about-carousel {
    max-width: 560px;
    margin: 0 auto 1rem;
    --swiper-theme-color: var(--global-theme-color);
    --swiper-navigation-size: 26px;
  }
  .about-carousel figure,
  .about-carousel picture {
    margin: 0;
    display: block;
  }
  .about-carousel swiper-slide img {
    width: 100%;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    border-radius: 0.6rem;
    display: block;
  }
  .about-carousel .caption {
    margin-top: 0.6rem;
    margin-bottom: 0;
  }
</style>

<p class="carousel-label">Some snapshots from second-year labs</p>
<swiper-container class="about-carousel" keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>
    {% include figure.liquid path="assets/img/lab1.jpg" class="img-fluid z-depth-1" %}
    <div class="caption">Dropwise addition of iodine chloride in DCM to pyridine in DCM at 0 ºC</div>
  </swiper-slide>
  <swiper-slide>
    {% include figure.liquid path="assets/img/lab2.jpg" class="img-fluid z-depth-1" %}
    <div class="caption">Dissolving iron chloride in degassed DMSO in nitrogen atmosphere</div>
  </swiper-slide>
  <swiper-slide>
    {% include figure.liquid path="assets/img/lab3.jpg" class="img-fluid z-depth-1" %}
    <div class="caption">Synthesised ligand for the synthesis investigation lab</div>
  </swiper-slide>
</swiper-container>

<p class="carousel-label">Some snapshots from a sailing competition</p>
<swiper-container class="about-carousel" keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>
    {% include figure.liquid path="assets/img/sailing1.jpg" class="img-fluid z-depth-1" %}
    <div class="caption">Switching boats at a competition</div>
  </swiper-slide>
  <swiper-slide>
    {% include figure.liquid path="assets/img/sailing2.jpg" class="img-fluid z-depth-1" %}
    <div class="caption">Sailing at Reading 2025 competition</div>
  </swiper-slide>
  <swiper-slide>
    {% include figure.liquid path="assets/img/sailing3.jpg" class="img-fluid z-depth-1" %}
    <div class="caption">Team picture from Reading 2025</div>
  </swiper-slide>
</swiper-container>
