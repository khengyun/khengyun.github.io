---
layout: about
title: about
permalink: /
subtitle: Combined M.S.–Ph.D. Student · AI Researcher & Engineer

profile:
  align: right
  image: prof_pic.jpg
  image_circular: true # crops the image to make it circular
  more_info: >
    <p>Sungkyunkwan University (SKKU)</p>
    <p>Electrical and Electronics Engineering</p>
    <p>South Korea</p>

selected_papers: false # keep the about page focused on the short biography
social: false # social icons are already displayed in the navbar

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<style>
  .education-list {
    display: grid;
    gap: 1.15rem;
    margin-top: 0.75rem;
  }

  .education-item {
    display: grid;
    grid-template-columns: 3.5rem minmax(0, 1fr);
    gap: 1rem;
    align-items: start;
  }

  .education-item__logo {
    display: flex;
    width: 3.5rem;
    height: 3.5rem;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.45rem;
    background: #fff;
  }

  .education-item__logo img {
    display: block;
    width: 100%;
    height: 100%;
    padding: 0.25rem;
    object-fit: contain;
  }

  .education-item__content h5 {
    margin: 0 0 0.35rem;
  }

  .education-item__content p {
    margin: 0 0 0.35rem;
  }

  .education-item__content p:last-child {
    margin-bottom: 0;
  }

  @media (max-width: 575px) {
    .education-item {
      grid-template-columns: 2.9rem minmax(0, 1fr);
      gap: 0.75rem;
    }

    .education-item__logo {
      width: 2.9rem;
      height: 2.9rem;
    }
  }
</style>

I am a combined M.S.–Ph.D. student at [Sungkyunkwan University](https://www.skku.edu/) (SKKU),
researching **intelligent surveillance systems** and **Edge AI**.

My background spans computer vision, multimodal learning, autonomous systems, medical imaging,
and LLM applications. I am interested in efficient, reproducible AI and open to
[research collaborations](mailto:khaangnguyeen@gmail.com).

## Education

<div class="education-list">
  <article class="education-item">
    <a
      class="education-item__logo"
      href="https://www.skku.edu/"
      target="_blank"
      rel="noopener noreferrer"
      aria-label="Visit Sungkyunkwan University"
    >
      <img src="{{ '/assets/img/education/skku.png' | relative_url }}" alt="Sungkyunkwan University logo">
    </a>
    <div class="education-item__content">
      <h5>Combined M.S.–Ph.D. · Electrical and Electronics Engineering</h5>
      <p><strong>Sungkyunkwan University (SKKU), South Korea</strong> · January 2026 — Present</p>
      <p>Fully funded scholarship. Research focus: intelligent surveillance systems, Edge AI, and efficient perception for edge devices.</p>
    </div>
  </article>

  <article class="education-item">
    <a
      class="education-item__logo"
      href="https://daihoc.fpt.edu.vn/"
      target="_blank"
      rel="noopener noreferrer"
      aria-label="Visit FPT University"
    >
      <img src="{{ '/assets/img/education/fpt-university.png' | relative_url }}" alt="FPT University logo">
    </a>
    <div class="education-item__content">
      <h5>B.S. · Software Engineering</h5>
      <p><strong>FPT University, Vietnam</strong> · September 2021 — April 2025</p>
      <p>Sub-major in Artificial Intelligence.</p>
    </div>
  </article>
</div>
