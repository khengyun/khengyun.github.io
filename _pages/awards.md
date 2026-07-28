---
layout: page
permalink: /awards/
title: awards
description: Selected awards and competition achievements.
nav: true
nav_order: 1
---

<style>
  .awards-layout {
    display: grid;
    grid-template-columns: 14rem minmax(0, 1fr);
    gap: clamp(2rem, 5vw, 4.5rem);
    align-items: start;
  }

  .awards-toc {
    position: sticky;
    top: 6rem;
    padding-right: 1.25rem;
    border-right: 1px solid var(--global-divider-color);
  }

  .awards-toc__title {
    margin: 0 0 0.75rem;
    color: var(--global-text-color);
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .awards-toc nav {
    display: grid;
    gap: 0.25rem;
  }

  .awards-toc a {
    display: grid;
    gap: 0.15rem;
    padding: 0.7rem 0.8rem;
    border-left: 3px solid transparent;
    color: var(--global-text-color);
    text-decoration: none;
    transition:
      border-color 160ms ease,
      background-color 160ms ease;
  }

  .awards-toc a:hover,
  .awards-toc a:focus {
    border-left-color: var(--global-theme-color);
    background: color-mix(in srgb, var(--global-theme-color) 8%, transparent);
  }

  .awards-toc a span {
    font-size: 0.95rem;
    font-weight: 650;
  }

  .awards-toc a small {
    color: var(--global-text-color-light);
    font-size: 0.78rem;
    line-height: 1.35;
  }

  .award-group {
    scroll-margin-top: 6rem;
    margin-bottom: 4rem;
  }

  .award-group:last-child {
    margin-bottom: 0;
  }

  .award-group__header {
    margin-bottom: 1rem;
    padding-bottom: 0.85rem;
    border-bottom: 1px solid var(--global-divider-color);
  }

  .award-group__date {
    margin: 0 0 0.25rem;
    color: var(--global-theme-color);
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }

  .award-group__header h2 {
    margin: 0;
    font-size: clamp(1.35rem, 2.3vw, 1.8rem);
    line-height: 1.25;
  }

  .award-entry {
    display: grid;
    grid-template-columns: minmax(11rem, 0.75fr) minmax(19rem, 1.25fr);
    gap: clamp(1.25rem, 3vw, 2rem);
    align-items: start;
    margin-bottom: 1.25rem;
    padding: clamp(1rem, 2.2vw, 1.5rem);
    border: 1px solid var(--global-divider-color);
    border-radius: 0.65rem;
    background: var(--global-card-bg-color);
  }

  .award-entry:last-child {
    margin-bottom: 0;
  }

  .award-entry__result {
    margin: 0 0 0.45rem;
    color: var(--global-theme-color);
    font-size: 0.8rem;
    font-weight: 750;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }

  .award-entry h3 {
    margin: 0 0 0.35rem;
    font-size: clamp(1.15rem, 2vw, 1.45rem);
    line-height: 1.3;
  }

  .award-entry__round {
    margin: 0 0 1rem;
    color: var(--global-text-color-light);
    font-weight: 600;
  }

  .award-entry__description {
    margin-bottom: 1rem;
    font-size: 0.95rem;
    line-height: 1.55;
  }

  .award-entry__source {
    display: inline-flex;
    gap: 0.35rem;
    align-items: center;
    font-size: 0.85rem;
    font-weight: 600;
  }

  .award-proof {
    display: flex;
    min-height: 12rem;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.45rem;
    background: #fff;
  }

  .award-proof img {
    display: block;
    width: 100%;
    max-height: 32rem;
    object-fit: contain;
  }

  .award-proof--text {
    min-height: 15rem;
    padding: 2rem;
    color: #1f2933;
    text-align: center;
    background:
      linear-gradient(135deg, rgb(255 255 255 / 92%), rgb(255 255 255 / 97%)),
      linear-gradient(135deg, #27ae60, #f2c94c);
  }

  .award-proof--text strong {
    display: block;
    margin-bottom: 0.65rem;
    color: #176b3a;
    font-size: clamp(1.3rem, 3vw, 2rem);
    letter-spacing: 0.05em;
  }

  .award-proof--text span {
    max-width: 22rem;
    line-height: 1.5;
  }

  @media (max-width: 991px) {
    .awards-layout {
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    .awards-toc {
      position: static;
      padding: 0 0 1.25rem;
      border-right: 0;
      border-bottom: 1px solid var(--global-divider-color);
    }

    .awards-toc nav {
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }
  }

  @media (max-width: 767px) {
    .awards-toc nav,
    .award-entry {
      grid-template-columns: 1fr;
    }

    .awards-toc a {
      border-left: 0;
      border-bottom: 2px solid transparent;
    }

    .awards-toc a:hover,
    .awards-toc a:focus {
      border-bottom-color: var(--global-theme-color);
    }
  }
</style>

<div class="awards-layout">
  <aside class="awards-toc" aria-label="Awards archive">
    <p class="awards-toc__title">Award archive</p>
    <nav>
      <a href="#december-2025">
        <span>December 2025</span>
        <small>Vietnam Association for Information Processing</small>
      </a>
      <a href="#september-2024">
        <span>September 2024</span>
        <small>MICCAI 2024</small>
      </a>
      <a href="#november-2022">
        <span>November 2022</span>
        <small>TECHFEST Vietnam 2022</small>
      </a>
    </nav>
  </aside>

  <div class="awards-detail">
    <section class="award-group" id="december-2025">
      <header class="award-group__header">
        <p class="award-group__date">December 2025</p>
        <h2>Vietnam Association for Information Processing</h2>
      </header>

      <article class="award-entry">
        <div>
          <p class="award-entry__result">First Prize</p>
          <h3>Vietnam Student AI Olympiad 2025</h3>
          <p class="award-entry__round">Southern Regional Round</p>
          <p class="award-entry__description">Awarded as a member of team FPTU HCM VOAI2.</p>
          <a
            class="award-entry__source"
            href="https://drive.google.com/file/d/1q1l6ecyxN2MNS8wxEC0Hg2RPOLKBhZ1_/view?usp=sharing"
            target="_blank"
            rel="noopener noreferrer"
          >
            Original certificate <span aria-hidden="true">↗</span>
          </a>
        </div>
        <a
          class="award-proof"
          href="{{ '/assets/img/awards/voai-2025-southern-regional.jpg' | relative_url }}"
          aria-label="View the First Prize certificate at full size"
        >
          <img
            src="{{ '/assets/img/awards/voai-2025-southern-regional.jpg' | relative_url }}"
            alt="First Prize certificate for the Vietnam Student AI Olympiad 2025 Southern Regional Round"
            loading="eager"
          >
        </a>
      </article>

      <article class="award-entry">
        <div>
          <p class="award-entry__result">Third Prize</p>
          <h3>Vietnam Student AI Olympiad 2025</h3>
          <p class="award-entry__round">National Final</p>
          <p class="award-entry__description">Awarded as a member of team FPTU HCM VOAI2.</p>
          <a
            class="award-entry__source"
            href="https://drive.google.com/file/d/12wkcV6XsfxGxCLpgp_7dBSgbfnjKhmxP/view?usp=sharing"
            target="_blank"
            rel="noopener noreferrer"
          >
            Original certificate <span aria-hidden="true">↗</span>
          </a>
        </div>
        <a
          class="award-proof"
          href="{{ '/assets/img/awards/voai-2025-national-final.jpg' | relative_url }}"
          aria-label="View the Third Prize certificate at full size"
        >
          <img
            src="{{ '/assets/img/awards/voai-2025-national-final.jpg' | relative_url }}"
            alt="Third Prize certificate for the Vietnam Student AI Olympiad 2025 National Final"
            loading="lazy"
          >
        </a>
      </article>
    </section>

    <section class="award-group" id="september-2024">
      <header class="award-group__header">
        <p class="award-group__date">September 2024</p>
        <h2>MICCAI 2024</h2>
      </header>

      <article class="award-entry">
        <div>
          <p class="award-entry__result">2nd Place</p>
          <h3>Endoscopic Vision Challenge</h3>
          <p class="award-entry__round">Surgical Tool Detection</p>
          <p class="award-entry__description">
            Achieved top-ranking performance in deep-learning-based surgical tool detection.
          </p>
          <a
            class="award-entry__source"
            href="https://drive.google.com/file/d/1gObfHQPloTfDrBh9BYe_ijECCkPxW-fW/view?usp=sharing"
            target="_blank"
            rel="noopener noreferrer"
          >
            Original certificate <span aria-hidden="true">↗</span>
          </a>
        </div>
        <a
          class="award-proof"
          href="{{ '/assets/img/awards/endoscopic-vision-2024-second-place.png' | relative_url }}"
          aria-label="View the 2nd Place certificate at full size"
        >
          <img
            src="{{ '/assets/img/awards/endoscopic-vision-2024-second-place.png' | relative_url }}"
            alt="2nd Place certificate for the Endoscopic Vision Challenge at MICCAI 2024"
            loading="lazy"
          >
        </a>
      </article>

      <article class="award-entry">
        <div>
          <p class="award-entry__result">Best Methodology Report</p>
          <h3>Endoscopic Vision Challenge</h3>
          <p class="award-entry__round">Surgical Tool Detection</p>
          <p class="award-entry__description">
            Recognized for research methodology and analysis in surgical tool detection.
          </p>
          <a
            class="award-entry__source"
            href="https://drive.google.com/file/d/1fGSSNtORj5X1_ScgEzRYOjRv2Ro3T8_A/view?usp=sharing"
            target="_blank"
            rel="noopener noreferrer"
          >
            Original certificate <span aria-hidden="true">↗</span>
          </a>
        </div>
        <a
          class="award-proof"
          href="{{ '/assets/img/awards/endoscopic-vision-2024-methodology.png' | relative_url }}"
          aria-label="View the Best Methodology Report certificate at full size"
        >
          <img
            src="{{ '/assets/img/awards/endoscopic-vision-2024-methodology.png' | relative_url }}"
            alt="Best Methodology Report certificate for the Endoscopic Vision Challenge at MICCAI 2024"
            loading="lazy"
          >
        </a>
      </article>
    </section>

    <section class="award-group" id="november-2022">
      <header class="award-group__header">
        <p class="award-group__date">November 2022</p>
        <h2>TECHFEST Vietnam 2022</h2>
      </header>

      <article class="award-entry">
        <div>
          <p class="award-entry__result">First Prize</p>
          <h3>Green Startup Creative Talent Contest</h3>
          <p class="award-entry__round">Green startup and circular economy</p>
          <p class="award-entry__description">
            Developed eco-friendly products from recycled coffee grounds.
          </p>
          <a
            class="award-entry__source"
            href="https://www.facebook.com/FPTU.CT.PCTSV/posts/pfbid0dCuTkZKiTD5sevLN6n7TFPoS7c89oc39c5PPDZ1sHyEmfUM7caAuryWQYis3iyjsl"
            target="_blank"
            rel="noopener noreferrer"
          >
            Event post <span aria-hidden="true">↗</span>
          </a>
        </div>
        <div class="award-proof award-proof--text" aria-label="TECHFEST Vietnam 2022 award summary">
          <span>
            <strong>TECHFEST VIETNAM 2022</strong>
            First Prize for an eco-friendly product concept using recycled coffee grounds.
          </span>
        </div>
      </article>
    </section>

  </div>
</div>
