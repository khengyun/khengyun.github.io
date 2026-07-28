---
layout: page
permalink: /awards/
title: awards
description: Selected awards and competition achievements.
nav: true
nav_order: 1
images:
  lightbox2: true
---

<style>
  .awards-layout {
    display: grid;
    grid-template-columns: 13rem minmax(0, 1fr);
    gap: clamp(2rem, 4vw, 3rem);
    align-items: start;
  }

  .awards-toc {
    position: sticky;
    top: 6rem;
    padding-right: 0.75rem;
  }

  .awards-toc nav {
    display: grid;
    gap: 1.25rem;
  }

  .awards-toc__period {
    display: grid;
    gap: 0.4rem;
    padding-left: 0.85rem;
    border-left: 1px solid var(--global-divider-color);
    transition: border-color 160ms ease;
  }

  .awards-toc__period.is-active {
    border-left-color: var(--global-theme-color);
  }

  .awards-toc__date {
    color: var(--global-text-color);
    font-size: 0.9rem;
    font-weight: 700;
    text-decoration: none;
    transition: color 160ms ease;
  }

  .awards-toc__period.is-active .awards-toc__date {
    color: var(--global-theme-color);
  }

  .awards-toc__groups {
    display: grid;
    gap: 0.15rem;
  }

  .awards-toc__group {
    padding: 0.15rem 0;
    color: var(--global-text-color-light);
    font-size: 0.75rem;
    line-height: 1.4;
    text-decoration: none;
    transition:
      color 160ms ease,
      font-weight 160ms ease;
  }

  .awards-toc__date:hover,
  .awards-toc__date:focus,
  .awards-toc__group:hover,
  .awards-toc__group:focus {
    color: var(--global-theme-color);
  }

  .awards-toc__group.is-active {
    color: var(--global-theme-color);
    font-weight: 600;
  }

  .award-period {
    scroll-margin-top: 7rem;
    margin-bottom: 3.5rem;
  }

  .award-period:last-child {
    margin-bottom: 0;
  }

  .award-period__date {
    margin: 0 0 0.35rem;
    color: var(--global-theme-color);
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }

  .award-group {
    scroll-margin-top: 7rem;
    margin-bottom: 2.75rem;
  }

  .award-group:last-child {
    margin-bottom: 0;
  }

  .award-group__header {
    margin-bottom: 0;
    padding-bottom: 0.75rem;
    border-bottom: 1px solid var(--global-divider-color);
  }

  .award-group__header h2 {
    margin: 0;
    font-size: clamp(1.3rem, 2.1vw, 1.65rem);
    line-height: 1.25;
  }

  .award-group__header--with-photo {
    display: grid;
    grid-template-columns: minmax(0, 1fr) 8rem;
    gap: 1rem;
    align-items: center;
  }

  .award-group__subtitle {
    margin: 0.35rem 0 0;
    color: var(--global-text-color-light);
    font-size: 0.9rem;
  }

  .award-group__photo {
    display: block;
    overflow: hidden;
    border: 1px solid var(--global-divider-color);
    border-radius: 0.45rem;
    aspect-ratio: 1;
    background: #fff;
  }

  .award-group__photo img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .award-entry {
    display: grid;
    grid-template-columns: minmax(14rem, 2fr) minmax(18rem, 3fr);
    gap: clamp(1.5rem, 3vw, 2.25rem);
    align-items: start;
    margin: 0;
    padding: clamp(1.2rem, 2.2vw, 1.5rem) 0;
    border-bottom: 1px solid var(--global-divider-color);
    background: transparent;
  }

  .award-entry:last-child {
    padding-bottom: 0;
    border-bottom: 0;
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
    font-size: clamp(1.15rem, 1.8vw, 1.35rem);
    line-height: 1.3;
  }

  .award-entry__round {
    margin: 0 0 0.8rem;
    color: var(--global-text-color-light);
    font-weight: 600;
  }

  .award-entry__description {
    margin-bottom: 0.85rem;
    font-size: 0.92rem;
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
    border-radius: 0.35rem;
    background: #fff;
    transition:
      border-color 160ms ease,
      opacity 160ms ease;
  }

  .award-proof:hover,
  .award-proof:focus {
    border-color: color-mix(in srgb, var(--global-theme-color) 45%, var(--global-divider-color));
    opacity: 0.94;
  }

  .award-proof img {
    display: block;
    width: 100%;
    max-height: 32rem;
    object-fit: contain;
  }

  .award-gallery {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0.75rem;
    align-items: start;
  }

  .award-gallery .award-proof {
    min-height: 0;
    aspect-ratio: 1;
  }

  .award-gallery .award-proof img {
    height: 100%;
    max-height: none;
    object-fit: cover;
  }

  .award-proof--contain img {
    object-fit: contain;
  }

  .award-gallery--three > .award-proof:last-child {
    grid-column: 1 / -1;
    width: calc(50% - 0.375rem);
    justify-self: center;
  }

  @media (max-width: 991px) {
    .awards-layout {
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    .awards-toc {
      position: static;
      padding: 0 0 1rem;
      border-right: 0;
      border-bottom: 1px solid var(--global-divider-color);
    }

    .awards-toc nav {
      grid-template-columns: repeat(4, minmax(0, 1fr));
    }
  }

  @media (max-width: 767px) {
    .award-entry {
      grid-template-columns: 1fr;
    }

    .awards-layout {
      gap: 1.5rem;
    }

    .awards-toc nav {
      gap: 0.5rem;
    }

    .awards-toc__period {
      display: block;
      padding: 0;
      border-left: 0;
    }

    .awards-toc__date {
      display: block;
      padding: 0.45rem 0.25rem;
      border-bottom: 2px solid transparent;
      text-align: center;
    }

    .awards-toc__period.is-active .awards-toc__date {
      border-bottom-color: var(--global-theme-color);
    }

    .awards-toc__groups {
      display: none;
    }

    .award-group__header--with-photo {
      grid-template-columns: minmax(0, 1fr) 6rem;
    }

    .award-entry {
      gap: 1rem;
    }

    .award-gallery {
      gap: 0.5rem;
    }

    .award-gallery--three > .award-proof:last-child {
      width: calc(50% - 0.25rem);
    }
  }
</style>

<div class="awards-layout">
  <aside class="awards-toc" aria-label="Awards archive">
    <nav>
      <div class="awards-toc__period">
        <a class="awards-toc__date" href="{{ '/awards/' | relative_url }}">2025</a>
        <div class="awards-toc__groups">
          <a class="awards-toc__group" href="#december-2025-vaip">
            Vietnam Association for Information Processing
          </a>
          <a class="awards-toc__group" href="#december-2025-vpbank">
            VPBank Technology Hackathon 2025
          </a>
          <a class="awards-toc__group" href="#september-2025-fpt-education">FPT Education</a>
          <a class="awards-toc__group" href="#april-2025-fpt-software">FPT Software</a>
        </div>
      </div>
      <div class="awards-toc__period">
        <a class="awards-toc__date" href="#2024">2024</a>
        <div class="awards-toc__groups">
          <a class="awards-toc__group" href="#september-2024-miccai">MICCAI 2024</a>
        </div>
      </div>
      <div class="awards-toc__period">
        <a class="awards-toc__date" href="#2023">2023</a>
        <div class="awards-toc__groups">
          <a class="awards-toc__group" href="#september-2023-fpt-education">FPT Education</a>
        </div>
      </div>
      <div class="awards-toc__period">
        <a class="awards-toc__date" href="#2022">2022</a>
        <div class="awards-toc__groups">
          <a class="awards-toc__group" href="#november-2022-techfest">TECHFEST Vietnam 2022</a>
        </div>
      </div>
    </nav>
  </aside>

  <div class="awards-detail">
    <section class="award-period" id="2025">
      <p class="award-period__date">2025</p>

      <section class="award-group" id="december-2025-vaip">
        <header class="award-group__header">
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
          <div class="award-gallery" aria-label="Southern Regional Round photo gallery">
            <a
              class="award-proof award-proof--contain"
              data-lightbox="voai-2025-southern"
              href="{{ '/assets/img/awards/voai-2025-southern-regional.jpg' | relative_url }}"
              aria-label="View the First Prize certificate at full size"
            >
              <img
                src="{{ '/assets/img/awards/voai-2025-southern-regional.jpg' | relative_url }}"
                alt="First Prize certificate for the Vietnam Student AI Olympiad 2025 Southern Regional Round"
                loading="eager"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="voai-2025-southern"
              href="{{ '/assets/img/awards/voai-2025-southern-regional-team.jpg' | relative_url }}"
              aria-label="View the FPTU HCM VOAI2 team photo at the Southern Regional Round"
            >
              <img
                src="{{ '/assets/img/awards/voai-2025-southern-regional-team.jpg' | relative_url }}"
                alt="Team FPTU HCM VOAI2 at the Vietnam Student AI Olympiad 2025 Southern Regional Round"
                loading="lazy"
              >
            </a>
          </div>
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
          <div class="award-gallery" aria-label="National Final photo gallery">
            <a
              class="award-proof award-proof--contain"
              data-lightbox="voai-2025-national"
              href="{{ '/assets/img/awards/voai-2025-national-final-award-ceremony.jpg' | relative_url }}"
              aria-label="View the National Final award ceremony photo at full size"
            >
              <img
                src="{{ '/assets/img/awards/voai-2025-national-final-award-ceremony.jpg' | relative_url }}"
                alt="Team FPTU HCM VOAI2 receiving awards at the Vietnam Student AI Olympiad 2025 National Final"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof award-proof--contain"
              data-lightbox="voai-2025-national"
              href="{{ '/assets/img/awards/voai-2025-national-final.jpg' | relative_url }}"
              aria-label="View the Third Prize certificate at full size"
            >
              <img
                src="{{ '/assets/img/awards/voai-2025-national-final.jpg' | relative_url }}"
                alt="Third Prize certificate for the Vietnam Student AI Olympiad 2025 National Final"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="voai-2025-national"
              href="{{ '/assets/img/awards/voai-2025-national-final-team.jpg' | relative_url }}"
              aria-label="View the team photo at the National Final"
            >
              <img
                src="{{ '/assets/img/awards/voai-2025-national-final-team.jpg' | relative_url }}"
                alt="Team members at the Vietnam Student AI Olympiad 2025 National Final"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof award-proof--contain"
              data-lightbox="voai-2025-national"
              href="{{ '/assets/img/awards/voai-2025-national-final-kit.jpg' | relative_url }}"
              aria-label="View the OLP AI 2025 contestant kit at full size"
            >
              <img
                src="{{ '/assets/img/awards/voai-2025-national-final-kit.jpg' | relative_url }}"
                alt="OLP AI 2025 contestant kit for Nguyen Hoang Khang of team FPTU HCM VOAI2"
                loading="lazy"
              >
            </a>
          </div>
        </article>
      </section>

      <section class="award-group" id="december-2025-vpbank">
        <header class="award-group__header">
          <h2>VPBank Technology Hackathon 2025</h2>
        </header>

        <article class="award-entry">
          <div>
            <p class="award-entry__result">Hackathon Star</p>
            <h3>Senior Track</h3>
            <p class="award-entry__round">Team Dream Come True</p>
            <p class="award-entry__description">
              Recognized for a solution that optimized 40% of testing costs.
            </p>
          </div>
          <div
            class="award-gallery"
            aria-label="VPBank Technology Hackathon 2025 photo gallery"
          >
            <a
              class="award-proof"
              data-lightbox="vpbank-2025"
              href="{{ '/assets/img/awards/vpbank-technology-hackathon-2025-awards-group.jpg' | relative_url }}"
              aria-label="View the VPBank Technology Hackathon 2025 awards group photo at full size"
            >
              <img
                src="{{ '/assets/img/awards/vpbank-technology-hackathon-2025-awards-group.jpg' | relative_url }}"
                alt="Award recipients at the VPBank Technology Hackathon 2025"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="vpbank-2025"
              href="{{ '/assets/img/awards/vpbank-technology-hackathon-2025.jpg' | relative_url }}"
              aria-label="View the Hackathon Star trophy photo at full size"
            >
              <img
                src="{{ '/assets/img/awards/vpbank-technology-hackathon-2025.jpg' | relative_url }}"
                alt="Hackathon Star trophy from the Senior Track at VPBank Technology Hackathon 2025"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="vpbank-2025"
              href="{{ '/assets/img/awards/vpbank-technology-hackathon-2025-team.jpg' | relative_url }}"
              aria-label="View the Dream Come True team photo at full size"
            >
              <img
                src="{{ '/assets/img/awards/vpbank-technology-hackathon-2025-team.jpg' | relative_url }}"
                alt="Team Dream Come True at the VPBank Technology Hackathon 2025 final competition round"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="vpbank-2025"
              href="{{ '/assets/img/awards/vpbank-technology-hackathon-2025-trophy-closeup.jpg' | relative_url }}"
              aria-label="View the Hackathon Star trophy close-up at full size"
            >
              <img
                src="{{ '/assets/img/awards/vpbank-technology-hackathon-2025-trophy-closeup.jpg' | relative_url }}"
                alt="Close-up of the Hackathon Star trophy from VPBank Technology Hackathon 2025"
                loading="lazy"
              >
            </a>
          </div>
        </article>
      </section>

      <section class="award-group" id="september-2025-fpt-education">
        <header class="award-group__header">
          <h2>FPT Education</h2>
        </header>

        <article class="award-entry">
          <div>
            <p class="award-entry__result">Third Place</p>
            <h3>FPT Hackathon 2025</h3>
            <p class="award-entry__round">Board A · Chip AI Logistics on Edge</p>
            <p class="award-entry__description">
              Won Third Place in Board A with Team One, representing FPT University Can Tho.
            </p>
            <a
              class="award-entry__source"
              href="https://www.facebook.com/share/1DCMaZuF4p/"
              target="_blank"
              rel="noopener noreferrer"
            >
              Event post <span aria-hidden="true">↗</span>
            </a>
          </div>
          <div
            class="award-gallery"
            aria-label="FPT Hackathon 2025 photo gallery"
          >
            <a
              class="award-proof"
              data-lightbox="fpt-hackathon-2025"
              href="{{ '/assets/img/awards/fpt-hackathon-2025-third-place.jpg' | relative_url }}"
              aria-label="View the Team One Third Place photo at full size"
            >
              <img
                src="{{ '/assets/img/awards/fpt-hackathon-2025-third-place.jpg' | relative_url }}"
                alt="Team One receiving the Third Place award in Board A at FPT Hackathon 2025"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof award-proof--contain"
              data-lightbox="fpt-hackathon-2025"
              href="{{ '/assets/img/awards/fpt-hackathon-2025-team-one-recognition.jpg' | relative_url }}"
              aria-label="View the Team One recognition image at full size"
            >
              <img
                src="{{ '/assets/img/awards/fpt-hackathon-2025-team-one-recognition.jpg' | relative_url }}"
                alt="Team One advancing to the FPT Hackathon 2025 National Final"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="fpt-hackathon-2025"
              href="{{ '/assets/img/awards/fpt-hackathon-2025-team-one.jpg' | relative_url }}"
              aria-label="View Team One at the FPT Hackathon 2025 final at full size"
            >
              <img
                src="{{ '/assets/img/awards/fpt-hackathon-2025-team-one.jpg' | relative_url }}"
                alt="Team One at the FPT Hackathon 2025 National Final"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="fpt-hackathon-2025"
              href="{{ '/assets/img/awards/fpt-hackathon-2025-working-session.jpg' | relative_url }}"
              aria-label="View Team One working at FPT Hackathon 2025 at full size"
            >
              <img
                src="{{ '/assets/img/awards/fpt-hackathon-2025-working-session.jpg' | relative_url }}"
                alt="Team One working on its solution during FPT Hackathon 2025"
                loading="lazy"
              >
            </a>
          </div>
        </article>
      </section>

      <section class="award-group" id="april-2025-fpt-software">
        <header class="award-group__header">
          <h2>FPT Software</h2>
        </header>

        <article class="award-entry">
          <div>
            <p class="award-entry__result">Top 1</p>
            <h3>FleziPT AI Champions</h3>
            <p class="award-entry__round">Hack The Future · Saigon 48</p>
            <p class="award-entry__description">
              Ranked first and received the AI Champion award, with a 20,000,000 VND prize.
            </p>
          </div>
          <div
            class="award-gallery"
            aria-label="FleziPT AI Champions photo gallery"
          >
            <a
              class="award-proof award-proof--contain"
              data-lightbox="flezipt-ai-champions-2025"
              href="{{ '/assets/img/awards/flezipt-ai-champions-2025-prize.jpg' | relative_url }}"
              aria-label="View the FleziPT AI Champion prize board at full size"
            >
              <img
                src="{{ '/assets/img/awards/flezipt-ai-champions-2025-prize.jpg' | relative_url }}"
                alt="FleziPT AI Champion prize board for 20,000,000 VND"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="flezipt-ai-champions-2025"
              href="{{ '/assets/img/awards/flezipt-ai-champions-2025-hackathon.jpg' | relative_url }}"
              aria-label="View the Hack The Future working session at full size"
            >
              <img
                src="{{ '/assets/img/awards/flezipt-ai-champions-2025-hackathon.jpg' | relative_url }}"
                alt="Participants working during the FleziPT AI Champions Hack The Future challenge"
                loading="lazy"
              >
            </a>
          </div>
        </article>
      </section>
    </section>

    <section class="award-period" id="2024">
      <p class="award-period__date">2024</p>

      <section class="award-group" id="september-2024-miccai">
        <header class="award-group__header award-group__header--with-photo">
          <div>
            <h2>MICCAI 2024</h2>
            <p class="award-group__subtitle">Endoscopic Vision Challenge team</p>
          </div>
          <a
            class="award-group__photo"
            data-lightbox="miccai-2024"
            href="{{ '/assets/img/awards/endoscopic-vision-2024-team.jpg' | relative_url }}"
            aria-label="View the Endoscopic Vision Challenge team photo at full size"
          >
            <img
              src="{{ '/assets/img/awards/endoscopic-vision-2024-team.jpg' | relative_url }}"
              alt="Endoscopic Vision Challenge team at MICCAI 2024"
              loading="lazy"
            >
          </a>
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
          class="award-proof award-proof--contain"
          data-lightbox="miccai-2024"
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
          class="award-proof award-proof--contain"
          data-lightbox="miccai-2024"
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
    </section>

    <section class="award-period" id="2023">
      <p class="award-period__date">2023</p>

      <section class="award-group" id="september-2023-fpt-education">
        <header class="award-group__header">
          <h2>FPT Education</h2>
        </header>

        <article class="award-entry">
          <div>
            <p class="award-entry__result">Consolation Prize</p>
            <h3>FPT Edu Digital Race 2023</h3>
            <p class="award-entry__round">National Final · Autonomous Vehicle AI</p>
            <p class="award-entry__description">
              Competed in an autonomous vehicle AI challenge, developing real-time object detection
              and navigation algorithms.
            </p>
            <a
              class="award-entry__source"
              href="https://www.facebook.com/FEExpSpace/posts/pfbid02CxAkNmgagwNbjqJKwLJnc5m7ss4nLXoAXE91JBrUenswC8ByNQdWrQK1jvWt84WGl"
              target="_blank"
              rel="noopener noreferrer"
            >
              Event post <span aria-hidden="true">↗</span>
            </a>
          </div>
          <div
            class="award-gallery award-gallery--three"
            aria-label="FPT Edu Digital Race 2023 photo gallery"
          >
            <a
              class="award-proof"
              data-lightbox="fpt-digital-race-2023"
              href="{{ '/assets/img/awards/fpt-edu-digital-race-2023-finalists.jpg' | relative_url }}"
              aria-label="View the FPT Edu Digital Race 2023 finalists photo at full size"
            >
              <img
                src="{{ '/assets/img/awards/fpt-edu-digital-race-2023-finalists.jpg' | relative_url }}"
                alt="Finalists and organizers at the FPT Edu Digital Race 2023 National Final"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof"
              data-lightbox="fpt-digital-race-2023"
              href="{{ '/assets/img/awards/fpt-edu-digital-race-2023-award-ceremony.jpg' | relative_url }}"
              aria-label="View the FPT Edu Digital Race 2023 award ceremony photo at full size"
            >
              <img
                src="{{ '/assets/img/awards/fpt-edu-digital-race-2023-award-ceremony.jpg' | relative_url }}"
                alt="Award recipients on stage at the FPT Edu Digital Race 2023 National Final"
                loading="lazy"
              >
            </a>
            <a
              class="award-proof award-proof--contain"
              data-lightbox="fpt-digital-race-2023"
              href="{{ '/assets/img/awards/fpt-edu-digital-race-2023-poster.jpg' | relative_url }}"
              aria-label="View the FPT Edu Digital Race 2023 National Final poster at full size"
            >
              <img
                src="{{ '/assets/img/awards/fpt-edu-digital-race-2023-poster.jpg' | relative_url }}"
                alt="FPT Edu Digital Race 2023 National Final poster"
                loading="lazy"
              >
            </a>
          </div>
        </article>
      </section>
    </section>

    <section class="award-period" id="2022">
      <p class="award-period__date">2022</p>

      <section class="award-group" id="november-2022-techfest">
        <header class="award-group__header">
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
          <a
            class="award-proof award-proof--contain"
            data-lightbox="techfest-2022"
            href="{{ '/assets/img/awards/techfest-2022-first-prize.jpg' | relative_url }}"
            aria-label="View the TECHFEST Vietnam 2022 First Prize image at full size"
          >
            <img
              src="{{ '/assets/img/awards/techfest-2022-first-prize.jpg' | relative_url }}"
              alt="First Prize award for the Green Creative Startup contest at TECHFEST Vietnam 2022"
              loading="lazy"
            >
          </a>
        </article>
      </section>
    </section>

  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", () => {
    const links = Array.from(document.querySelectorAll(".awards-toc__group"));
    const sections = links
      .map((link) => {
        const id = link.getAttribute("href")?.slice(1);
        const section = id ? document.getElementById(id) : null;
        return section ? { link, section } : null;
      })
      .filter(Boolean);

    if (!sections.length) return;

    let scheduled = false;

    const updateActiveSection = () => {
      const marker = window.scrollY + Math.min(window.innerHeight * 0.28, 180);
      let active = sections[0];

      sections.forEach((item) => {
        if (item.section.offsetTop <= marker) active = item;
      });

      links.forEach((link) => {
        const isActive = link === active.link;
        link.classList.toggle("is-active", isActive);
        if (isActive) {
          link.setAttribute("aria-current", "location");
        } else {
          link.removeAttribute("aria-current");
        }
      });

      document.querySelectorAll(".awards-toc__period").forEach((period) => {
        period.classList.toggle("is-active", period.contains(active.link));
      });

      scheduled = false;
    };

    const scheduleUpdate = () => {
      if (scheduled) return;
      scheduled = true;
      window.requestAnimationFrame(updateActiveSection);
    };

    window.addEventListener("scroll", scheduleUpdate, { passive: true });
    window.addEventListener("resize", scheduleUpdate);
    updateActiveSection();
  });
</script>
