<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Runner's Fueling Guide — Fuel Smart, Run Strong</title>
  <meta name="description" content="Visual fueling guide for runners showing when and what to eat before, during, and after easy runs, intervals, long runs, and race day efforts.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300..700;1,9..40,300..700&family=DM+Serif+Display&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    /* ============================================
       DESIGN TOKENS
       ============================================ */
    :root {
      --color-bg: #faf9f7;
      --color-bg-warm: #f5f2ed;
      --color-surface: #ffffff;
      --color-text: #1a1a1a;
      --color-text-secondary: #5c5c5c;
      --color-text-muted: #8a8a8a;
      --color-border: #e5e2dc;
      --color-border-light: #eeeae4;

      /* Run type accent colors */
      --color-easy: #4a9e6e;
      --color-easy-bg: #eaf5ef;
      --color-easy-light: #d4ebdf;
      --color-intervals: #c75a2a;
      --color-intervals-bg: #fdf0ea;
      --color-intervals-light: #f9ddd0;
      --color-long: #3a73b5;
      --color-long-bg: #e9f0f9;
      --color-long-light: #d0e0f2;
      --color-race: #8b5fbf;
      --color-race-bg: #f2ecf9;
      --color-race-light: #e2d5f0;

      /* GI colors */
      --gi-low: #4a9e6e;
      --gi-mod: #d4a017;
      --gi-high: #c75a2a;

      /* Typography */
      --font-sans: 'DM Sans', system-ui, -apple-system, sans-serif;
      --font-serif: 'DM Serif Display', Georgia, serif;
      --font-mono: 'JetBrains Mono', monospace;

      /* Spacing */
      --space-xs: 0.25rem;
      --space-sm: 0.5rem;
      --space-md: 1rem;
      --space-lg: 1.5rem;
      --space-xl: 2rem;
      --space-2xl: 3rem;
      --space-3xl: 4rem;
      --space-4xl: 6rem;

      /* Radius */
      --radius-sm: 6px;
      --radius-md: 10px;
      --radius-lg: 16px;
      --radius-xl: 24px;
    }

    /* ============================================
       RESET & BASE
       ============================================ */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html {
      font-size: 16px;
      scroll-behavior: smooth;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    body {
      font-family: var(--font-sans);
      background: var(--color-bg);
      color: var(--color-text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ============================================
       LAYOUT
       ============================================ */
    .container {
      max-width: 1080px;
      margin: 0 auto;
      padding: 0 var(--space-xl);
    }

    /* ============================================
       HEADER
       ============================================ */
    .hero {
      padding: var(--space-4xl) 0 var(--space-3xl);
      text-align: center;
      position: relative;
    }

    .hero::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 60px;
      height: 3px;
      background: var(--color-text);
      border-radius: 2px;
    }

    .hero-label {
      font-family: var(--font-mono);
      font-size: 0.75rem;
      font-weight: 500;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--color-text-muted);
      margin-bottom: var(--space-md);
    }

    .hero h1 {
      font-family: var(--font-serif);
      font-size: clamp(2.2rem, 5vw, 3.4rem);
      line-height: 1.15;
      letter-spacing: -0.02em;
      margin-bottom: var(--space-lg);
    }

    .hero p {
      font-size: 1.1rem;
      color: var(--color-text-secondary);
      max-width: 600px;
      margin: 0 auto;
      line-height: 1.7;
    }

    /* ============================================
       KEY PRINCIPLE BANNER
       ============================================ */
    .principle {
      background: var(--color-text);
      color: var(--color-bg);
      border-radius: var(--radius-lg);
      padding: var(--space-xl) var(--space-2xl);
      margin: var(--space-3xl) 0;
      display: flex;
      align-items: flex-start;
      gap: var(--space-lg);
    }

    .principle-icon {
      font-size: 1.6rem;
      flex-shrink: 0;
      margin-top: 2px;
    }

    .principle h2 {
      font-family: var(--font-sans);
      font-size: 1rem;
      font-weight: 600;
      letter-spacing: 0.02em;
      margin-bottom: var(--space-xs);
      color: rgba(255,255,255,0.6);
      text-transform: uppercase;
      font-size: 0.75rem;
      letter-spacing: 0.1em;
    }

    .principle p {
      font-size: 1.05rem;
      line-height: 1.65;
      color: rgba(255,255,255,0.92);
    }

    .principle strong {
      color: #fff;
    }

    /* ============================================
       GI LEGEND
       ============================================ */
    .legend {
      display: flex;
      justify-content: center;
      gap: var(--space-xl);
      flex-wrap: wrap;
      margin-bottom: var(--space-3xl);
      padding: var(--space-lg) var(--space-xl);
      background: var(--color-surface);
      border: 1px solid var(--color-border);
      border-radius: var(--radius-md);
    }

    .legend-title {
      width: 100%;
      text-align: center;
      font-family: var(--font-mono);
      font-size: 0.7rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--color-text-muted);
      margin-bottom: var(--space-sm);
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: var(--space-sm);
      font-size: 0.88rem;
      color: var(--color-text-secondary);
    }

    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      flex-shrink: 0;
    }

    .legend-dot.low { background: var(--gi-low); }
    .legend-dot.mod { background: var(--gi-mod); }
    .legend-dot.high { background: var(--gi-high); }

    /* ============================================
       SECTION HEADER
       ============================================ */
    .section-header {
      margin-bottom: var(--space-2xl);
    }

    .section-header h2 {
      font-family: var(--font-serif);
      font-size: clamp(1.6rem, 3.5vw, 2.2rem);
      letter-spacing: -0.01em;
      margin-bottom: var(--space-sm);
    }

    .section-header p {
      color: var(--color-text-secondary);
      font-size: 1rem;
    }

    /* ============================================
       RUN TYPE CARDS
       ============================================ */
    .run-type {
      margin-bottom: var(--space-4xl);
      scroll-margin-top: 2rem;
    }

    .run-card {
      border: 1px solid var(--color-border);
      border-radius: var(--radius-lg);
      overflow: hidden;
      background: var(--color-surface);
      box-shadow: 0 1px 3px rgba(0,0,0,0.04), 0 8px 24px rgba(0,0,0,0.03);
    }

    .run-card-header {
      padding: var(--space-xl) var(--space-2xl);
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: var(--space-md);
    }

    .run-card-header.easy { background: var(--color-easy-bg); border-bottom: 2px solid var(--color-easy-light); }
    .run-card-header.intervals { background: var(--color-intervals-bg); border-bottom: 2px solid var(--color-intervals-light); }
    .run-card-header.long { background: var(--color-long-bg); border-bottom: 2px solid var(--color-long-light); }
    .run-card-header.race { background: var(--color-race-bg); border-bottom: 2px solid var(--color-race-light); }

    .run-card-title {
      display: flex;
      align-items: center;
      gap: var(--space-md);
    }

    .run-icon {
      width: 48px;
      height: 48px;
      border-radius: var(--radius-md);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.4rem;
      color: #fff;
      flex-shrink: 0;
    }

    .run-icon.easy { background: var(--color-easy); }
    .run-icon.intervals { background: var(--color-intervals); }
    .run-icon.long { background: var(--color-long); }
    .run-icon.race { background: var(--color-race); }

    .run-card-title h3 {
      font-family: var(--font-serif);
      font-size: 1.4rem;
      letter-spacing: -0.01em;
    }

    .run-card-title span {
      display: block;
      font-family: var(--font-sans);
      font-size: 0.82rem;
      font-weight: 400;
      color: var(--color-text-secondary);
      margin-top: 2px;
    }

    .run-meta {
      display: flex;
      gap: var(--space-md);
      flex-wrap: wrap;
    }

    .run-meta-tag {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      letter-spacing: 0.04em;
      padding: 5px 12px;
      border-radius: 100px;
      background: rgba(255,255,255,0.7);
      border: 1px solid rgba(0,0,0,0.08);
      color: var(--color-text-secondary);
      white-space: nowrap;
    }

    /* ============================================
       TIMELINE
       ============================================ */
    .timeline {
      padding: var(--space-xl) var(--space-2xl) var(--space-2xl);
      display: grid;
      gap: 0;
      position: relative;
    }

    .timeline-phase {
      display: grid;
      grid-template-columns: 140px 1fr;
      gap: 0;
      position: relative;
      min-height: 100px;
    }

    .timeline-phase:not(:last-child) .timeline-content {
      border-bottom: 1px solid var(--color-border-light);
    }

    .timeline-label {
      position: relative;
      padding: var(--space-lg) var(--space-xl) var(--space-lg) 0;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      text-align: right;
    }

    .timeline-label::after {
      content: '';
      position: absolute;
      right: 0;
      top: 0;
      bottom: 0;
      width: 2px;
      background: var(--color-border);
    }

    .timeline-phase:first-child .timeline-label::after { top: 28px; }
    .timeline-phase:last-child .timeline-label::after { bottom: calc(100% - 28px); }

    .timeline-dot {
      position: absolute;
      right: -5px;
      top: 26px;
      width: 12px;
      height: 12px;
      border-radius: 50%;
      border: 2px solid var(--color-surface);
      z-index: 1;
    }

    .easy .timeline-dot { background: var(--color-easy); }
    .intervals .timeline-dot { background: var(--color-intervals); }
    .long .timeline-dot { background: var(--color-long); }
    .race .timeline-dot { background: var(--color-race); }

    .timeline-time {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      font-weight: 500;
      letter-spacing: 0.03em;
      color: var(--color-text-muted);
      text-transform: uppercase;
    }

    .timeline-phase-name {
      font-weight: 600;
      font-size: 0.88rem;
      margin-top: 2px;
      color: var(--color-text);
    }

    .timeline-content {
      padding: var(--space-lg) 0 var(--space-lg) var(--space-xl);
    }

    /* ============================================
       FUEL ITEMS
       ============================================ */
    .fuel-items {
      display: flex;
      flex-direction: column;
      gap: var(--space-md);
    }

    .fuel-item {
      display: flex;
      gap: var(--space-md);
      align-items: flex-start;
    }

    .fuel-gi {
      flex-shrink: 0;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      margin-top: 7px;
    }

    .fuel-gi.low { background: var(--gi-low); }
    .fuel-gi.mod { background: var(--gi-mod); }
    .fuel-gi.high { background: var(--gi-high); }

    .fuel-text {
      flex: 1;
    }

    .fuel-what {
      font-size: 0.92rem;
      font-weight: 500;
      color: var(--color-text);
      line-height: 1.4;
    }

    .fuel-why {
      font-size: 0.82rem;
      color: var(--color-text-muted);
      line-height: 1.5;
      margin-top: 2px;
    }

    .fuel-example {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--color-text-secondary);
      background: var(--color-bg-warm);
      padding: 3px 10px;
      border-radius: 100px;
      margin-top: 6px;
    }

    /* Phase emphasis: the run itself */
    .timeline-phase.run-phase .timeline-content {
      background: var(--color-bg-warm);
      border-radius: 0 var(--radius-md) var(--radius-md) 0;
      margin-right: calc(-1 * var(--space-2xl));
      padding-right: var(--space-2xl);
    }

    .run-activity {
      display: flex;
      align-items: center;
      gap: var(--space-sm);
      font-size: 0.88rem;
      font-weight: 600;
      margin-bottom: var(--space-sm);
    }

    .run-activity-icon {
      font-size: 1.1rem;
    }

    /* ============================================
       NOTES / CALLOUTS
       ============================================ */
    .run-card-footer {
      padding: var(--space-lg) var(--space-2xl);
      background: var(--color-bg);
      border-top: 1px solid var(--color-border-light);
      display: flex;
      align-items: flex-start;
      gap: var(--space-md);
      font-size: 0.85rem;
      color: var(--color-text-secondary);
      line-height: 1.6;
    }

    .run-card-footer strong {
      color: var(--color-text);
    }

    .footer-icon {
      flex-shrink: 0;
      font-size: 1rem;
      margin-top: 1px;
    }

    /* ============================================
       BLOOD SUGAR CONTEXT SECTION
       ============================================ */
    .context-section {
      margin: var(--space-3xl) 0;
    }

    .context-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: var(--space-lg);
      margin-top: var(--space-xl);
    }

    .context-card {
      background: var(--color-surface);
      border: 1px solid var(--color-border);
      border-radius: var(--radius-md);
      padding: var(--space-xl);
    }

    .context-card-icon {
      font-size: 1.5rem;
      margin-bottom: var(--space-md);
    }

    .context-card h3 {
      font-family: var(--font-sans);
      font-weight: 600;
      font-size: 1rem;
      margin-bottom: var(--space-sm);
    }

    .context-card p {
      font-size: 0.88rem;
      color: var(--color-text-secondary);
      line-height: 1.65;
    }

    /* ============================================
       NAV PILLS
       ============================================ */
    .nav-pills {
      display: flex;
      gap: var(--space-sm);
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: var(--space-3xl);
      position: sticky;
      top: 0;
      z-index: 100;
      padding: var(--space-md) 0;
      background: linear-gradient(to bottom, var(--color-bg) 70%, transparent);
    }

    .nav-pill {
      font-family: var(--font-sans);
      font-size: 0.82rem;
      font-weight: 500;
      padding: 8px 18px;
      border-radius: 100px;
      border: 1px solid var(--color-border);
      background: var(--color-surface);
      cursor: pointer;
      transition: all 0.2s ease;
      text-decoration: none;
      color: var(--color-text-secondary);
    }

    .nav-pill:hover {
      border-color: var(--color-text);
      color: var(--color-text);
    }

    .nav-pill.easy:hover, .nav-pill.easy.active { background: var(--color-easy); color: #fff; border-color: var(--color-easy); }
    .nav-pill.intervals:hover, .nav-pill.intervals.active { background: var(--color-intervals); color: #fff; border-color: var(--color-intervals); }
    .nav-pill.long:hover, .nav-pill.long.active { background: var(--color-long); color: #fff; border-color: var(--color-long); }
    .nav-pill.race:hover, .nav-pill.race.active { background: var(--color-race); color: #fff; border-color: var(--color-race); }
    .nav-pill.weekly:hover, .nav-pill.weekly.active { background: var(--color-text); color: #fff; border-color: var(--color-text); }

    /* ============================================
       WEEKLY TIMELINE
       ============================================ */
    .weekly-section {
      margin-bottom: var(--space-4xl);
      scroll-margin-top: 2rem;
    }

    .weekly-card {
      border: 1px solid var(--color-border);
      border-radius: var(--radius-lg);
      overflow: hidden;
      background: var(--color-surface);
      box-shadow: 0 1px 3px rgba(0,0,0,0.04), 0 8px 24px rgba(0,0,0,0.03);
    }

    .weekly-card-header {
      padding: var(--space-xl) var(--space-2xl);
      background: var(--color-bg-warm);
      border-bottom: 2px solid var(--color-border-light);
      display: flex;
      align-items: center;
      gap: var(--space-md);
    }

    .weekly-card-header .run-icon {
      background: var(--color-text);
    }

    .weekly-card-header h3 {
      font-family: var(--font-serif);
      font-size: 1.4rem;
    }

    .weekly-card-header h3 span {
      display: block;
      font-family: var(--font-sans);
      font-size: 0.82rem;
      font-weight: 400;
      color: var(--color-text-secondary);
      margin-top: 2px;
    }

    /* Bar chart */
    .carb-chart {
      padding: var(--space-2xl);
      border-bottom: 1px solid var(--color-border-light);
    }

    .carb-chart-label {
      font-family: var(--font-mono);
      font-size: 0.7rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--color-text-muted);
      margin-bottom: var(--space-lg);
      text-align: center;
    }

    .chart-container {
      display: flex;
      align-items: flex-end;
      gap: 0;
      height: 200px;
      position: relative;
      padding-bottom: 36px;
    }

    .chart-col {
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0;
      height: 100%;
      position: relative;
      justify-content: flex-end;
      padding: 0 4px;
    }

    .chart-bar-wrapper {
      flex: 1;
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-items: center;
      position: relative;
    }

    .chart-bar {
      width: 100%;
      max-width: 64px;
      border-radius: var(--radius-sm) var(--radius-sm) 0 0;
      position: relative;
      transition: height 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
      min-height: 4px;
    }

    .chart-bar-value {
      position: absolute;
      top: -22px;
      left: 50%;
      transform: translateX(-50%);
      font-family: var(--font-mono);
      font-size: 0.68rem;
      font-weight: 500;
      color: var(--color-text-secondary);
      white-space: nowrap;
    }

    .chart-bar.rest { background: #d4d0c8; }
    .chart-bar.easy-bar { background: var(--color-easy); opacity: 0.7; }
    .chart-bar.intervals-bar { background: var(--color-intervals); }
    .chart-bar.long-bar { background: var(--color-long); }
    .chart-bar.prime-bar { background: var(--color-long); opacity: 0.5; }
    .chart-bar.recovery-bar { background: var(--color-easy); opacity: 0.5; }

    .chart-day-label {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      font-weight: 500;
      color: var(--color-text-secondary);
      padding-top: 10px;
      text-align: center;
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
    }

    .chart-workout-label {
      font-size: 0.68rem;
      color: var(--color-text-muted);
      text-align: center;
      margin-top: 2px;
      line-height: 1.3;
    }

    .chart-day-label.has-workout {
      font-weight: 600;
      color: var(--color-text);
    }

    /* Scale lines */
    .chart-scale {
      position: absolute;
      left: 0;
      right: 0;
      border-top: 1px dashed var(--color-border-light);
      pointer-events: none;
    }

    .chart-scale-label {
      position: absolute;
      left: -4px;
      top: -8px;
      font-family: var(--font-mono);
      font-size: 0.6rem;
      color: var(--color-border);
      transform: translateX(-100%);
    }

    /* Day detail cards */
    .weekly-days {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 0;
    }

    .day-card {
      padding: var(--space-lg) var(--space-md);
      border-right: 1px solid var(--color-border-light);
      position: relative;
    }

    .day-card:last-child { border-right: none; }

    .day-card-day {
      font-family: var(--font-mono);
      font-size: 0.68rem;
      font-weight: 500;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--color-text-muted);
      margin-bottom: 2px;
    }

    .day-card-type {
      font-weight: 600;
      font-size: 0.82rem;
      margin-bottom: var(--space-sm);
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .day-card-type-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      flex-shrink: 0;
    }

    .day-card-carb {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      font-weight: 500;
      margin-bottom: var(--space-sm);
      padding: 4px 8px;
      border-radius: var(--radius-sm);
      display: inline-block;
    }

    .day-card-carb.low { background: #f0edea; color: var(--color-text-secondary); }
    .day-card-carb.moderate { background: var(--color-easy-bg); color: #3a7d55; }
    .day-card-carb.high { background: var(--color-intervals-bg); color: var(--color-intervals); }
    .day-card-carb.highest { background: var(--color-long-bg); color: var(--color-long); }

    .day-card-meals {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    .day-card-meals li {
      font-size: 0.75rem;
      color: var(--color-text-secondary);
      line-height: 1.45;
      padding-left: 12px;
      position: relative;
    }

    .day-card-meals li::before {
      content: '';
      position: absolute;
      left: 0;
      top: 6px;
      width: 5px;
      height: 5px;
      border-radius: 50%;
      background: var(--color-border);
    }

    .day-card-meals li strong {
      color: var(--color-text);
      font-weight: 600;
    }

    .day-card.workout-day {
      background: var(--color-bg-warm);
    }

    .day-card.prime-day {
      background: #f6f9fd;
    }

    /* Weekly callout */
    .weekly-callout {
      padding: var(--space-xl) var(--space-2xl);
      border-top: 1px solid var(--color-border-light);
      display: flex;
      flex-direction: column;
      gap: var(--space-lg);
    }

    .weekly-callout-item {
      display: flex;
      align-items: flex-start;
      gap: var(--space-md);
    }

    .weekly-callout-item .footer-icon {
      flex-shrink: 0;
      font-size: 1rem;
      margin-top: 2px;
    }

    .weekly-callout-item p {
      font-size: 0.85rem;
      color: var(--color-text-secondary);
      line-height: 1.6;
    }

    .weekly-callout-item p strong {
      color: var(--color-text);
    }

    /* Responsive weekly */
    @media (max-width: 900px) {
      .weekly-days {
        grid-template-columns: repeat(4, 1fr);
      }
      .day-card { border-bottom: 1px solid var(--color-border-light); }
    }

    @media (max-width: 600px) {
      .weekly-days {
        grid-template-columns: repeat(2, 1fr);
      }
      .chart-container { height: 150px; }
      .chart-bar-value { font-size: 0.6rem; }
      .carb-chart { padding: var(--space-lg) var(--space-md); }
      .weekly-callout { padding: var(--space-lg); }
    }

    @media (max-width: 480px) {
      .weekly-days {
        grid-template-columns: 1fr;
      }
    }

    /* ============================================
       FOOTER
       ============================================ */
    .page-footer {
      text-align: center;
      padding: var(--space-3xl) 0;
      border-top: 1px solid var(--color-border);
      margin-top: var(--space-4xl);
    }

    .page-footer p {
      font-size: 0.82rem;
      color: var(--color-text-muted);
      line-height: 1.7;
      max-width: 500px;
      margin: 0 auto;
    }

    /* ============================================
       RESPONSIVE
       ============================================ */
    @media (max-width: 720px) {
      .container { padding: 0 var(--space-md); }
      .hero { padding: var(--space-2xl) 0 var(--space-xl); }

      .principle {
        flex-direction: column;
        padding: var(--space-lg);
      }

      .run-card-header {
        padding: var(--space-lg);
      }

      .timeline {
        padding: var(--space-lg) var(--space-md);
      }

      .timeline-phase {
        grid-template-columns: 100px 1fr;
      }

      .timeline-label {
        padding: var(--space-md) var(--space-md) var(--space-md) 0;
      }

      .timeline-content {
        padding: var(--space-md) 0 var(--space-md) var(--space-md);
      }

      .timeline-phase.run-phase .timeline-content {
        margin-right: calc(-1 * var(--space-md));
        padding-right: var(--space-md);
      }

      .run-card-footer {
        padding: var(--space-lg);
      }

      .run-meta-tag { font-size: 0.65rem; }

      .legend { gap: var(--space-md); padding: var(--space-md); }
    }

    @media (max-width: 480px) {
      .timeline-phase {
        grid-template-columns: 1fr;
      }

      .timeline-label {
        align-items: flex-start;
        text-align: left;
        padding: var(--space-sm) 0 0 0;
      }

      .timeline-label::after { display: none; }
      .timeline-dot { display: none; }

      .timeline-content {
        padding: var(--space-sm) 0 var(--space-lg) 0;
      }

      .timeline-phase.run-phase .timeline-content {
        margin-right: 0;
        border-radius: var(--radius-md);
        padding: var(--space-md);
      }

      .nav-pills { gap: 6px; }
      .nav-pill { font-size: 0.75rem; padding: 6px 14px; }
    }

    /* ============================================
       ANIMATIONS
       ============================================ */
    .run-type {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.5s ease, transform 0.5s ease;
    }

    .run-type.visible {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>
<body>

  <div class="container">

    <!-- ======== HERO ======== -->
    <header class="hero">
      <p class="hero-label">Runner's Fueling Guide</p>
      <h1>Fuel Smart, Run Strong</h1>
      <p>What you eat — and <em>when</em> you eat it — changes based on the workout. Here's how to balance performance fueling with blood sugar health across every type of run.</p>
    </header>

    <!-- ======== CORE PRINCIPLE ======== -->
    <div class="principle">
      <span class="principle-icon">⚡</span>
      <div>
        <h2>The Core Principle</h2>
        <p>During exercise, your muscles absorb glucose through <strong>insulin-independent pathways</strong> (GLUT4 transporters). This means carbs consumed around hard workouts behave very differently than carbs eaten at rest. <strong>Fuel hard around hard work. Eat controlled the rest of the time.</strong></p>
      </div>
    </div>

    <!-- ======== GI LEGEND ======== -->
    <div class="legend">
      <span class="legend-title">Glycemic Index Guide</span>
      <div class="legend-item">
        <span class="legend-dot low"></span>
        Low GI — Slow, sustained energy
      </div>
      <div class="legend-item">
        <span class="legend-dot mod"></span>
        Moderate GI — Balanced absorption
      </div>
      <div class="legend-item">
        <span class="legend-dot high"></span>
        High GI — Rapid fuel delivery
      </div>
    </div>

    <!-- ======== NAV ======== -->
    <nav class="nav-pills">
      <a href="#easy" class="nav-pill easy">Easy Run</a>
      <a href="#intervals" class="nav-pill intervals">Intervals & Tempo</a>
      <a href="#long" class="nav-pill long">Long Run</a>
      <a href="#race" class="nav-pill race">Race Day</a>
      <a href="#weekly" class="nav-pill weekly">Weekly Plan</a>
    </nav>

    <!-- ============================================================
         EASY RUN
         ============================================================ -->
    <section class="run-type" id="easy">
      <div class="run-card">
        <div class="run-card-header easy">
          <div class="run-card-title">
            <div class="run-icon easy">🏃</div>
            <div>
              <h3>Easy Run</h3>
              <span>Recovery jogs, base-building aerobic runs</span>
            </div>
          </div>
          <div class="run-meta">
            <span class="run-meta-tag">30–60 min</span>
            <span class="run-meta-tag">Low intensity</span>
            <span class="run-meta-tag">Carb needs: Low</span>
          </div>
        </div>

        <div class="timeline easy">
          <!-- PRE -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">2–3 hrs before</span>
              <span class="timeline-phase-name">Pre-Run</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Normal balanced meal — no special loading needed</div>
                    <div class="fuel-why">Fat + protein + fiber to keep blood sugar flat. Your glycogen stores easily cover this effort.</div>
                    <span class="fuel-example">e.g. Eggs, avocado toast on whole grain</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Or run fasted if tolerated</div>
                    <div class="fuel-why">Easy effort can be sustained on existing glycogen + fat oxidation. Trains metabolic flexibility.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- DURING -->
          <div class="timeline-phase run-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">During</span>
              <span class="timeline-phase-name">The Run</span>
            </div>
            <div class="timeline-content">
              <div class="run-activity">
                <span class="run-activity-icon">🟢</span>
                30–60 minutes easy pace
              </div>
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low" style="background:var(--color-text-muted)"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Water only</div>
                    <div class="fuel-why">No fueling needed. Your body has 90+ minutes of glycogen available, and fat oxidation handles the rest at this intensity.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- POST -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">Within 1–2 hrs</span>
              <span class="timeline-phase-name">Recovery</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Regular whole-food meal — no rush to reload</div>
                    <div class="fuel-why">Glycogen depletion is minimal. Eat your next normal meal with protein and veggies first.</div>
                    <span class="fuel-example">e.g. Salad with chicken, lentils, olive oil dressing</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="run-card-footer">
          <span class="footer-icon">💡</span>
          <p><strong>Blood sugar win:</strong> Easy runs are your best opportunity to keep carbs low and controlled. Lean into whole foods, protein, and fiber on these days — save the high-carb fueling for workouts that actually demand it.</p>
        </div>
      </div>
    </section>

    <!-- ============================================================
         INTERVALS / TEMPO
         ============================================================ -->
    <section class="run-type" id="intervals">
      <div class="run-card">
        <div class="run-card-header intervals">
          <div class="run-card-title">
            <div class="run-icon intervals">⚡</div>
            <div>
              <h3>Intervals & Tempo</h3>
              <span>Track repeats, threshold runs, fartleks</span>
            </div>
          </div>
          <div class="run-meta">
            <span class="run-meta-tag">45–75 min</span>
            <span class="run-meta-tag">High intensity</span>
            <span class="run-meta-tag">Carb needs: Moderate</span>
          </div>
        </div>

        <div class="timeline intervals">
          <!-- PRE -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">2–3 hrs before</span>
              <span class="timeline-phase-name">Pre-Run</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Low-GI carbs with protein — top off glycogen gently</div>
                    <div class="fuel-why">Sustained release avoids an insulin spike before high-intensity work, which would blunt fat oxidation during warm-up.</div>
                    <span class="fuel-example">e.g. Oatmeal with nuts and berries, or sweet potato + eggs</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- 30 MIN BEFORE -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">30 min before</span>
              <span class="timeline-phase-name">Top-Up</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi mod"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Small, easy-digesting carb if needed</div>
                    <div class="fuel-why">Optional — only if your pre-run meal was 3+ hours ago. Keep it small to avoid gut distress during hard efforts.</div>
                    <span class="fuel-example">e.g. Half a banana, a few dates</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- DURING -->
          <div class="timeline-phase run-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">During</span>
              <span class="timeline-phase-name">The Workout</span>
            </div>
            <div class="timeline-content">
              <div class="run-activity">
                <span class="run-activity-icon">🟠</span>
                45–75 min with hard intervals
              </div>
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi high"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Sports drink during if session exceeds 60 min</div>
                    <div class="fuel-why">Muscles are pulling glucose directly — insulin-independent. High-GI is ideal here and won't spike blood sugar the way it would at rest.</div>
                    <span class="fuel-example">e.g. Electrolyte drink with 30g carbs, or half a gel between sets</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low" style="background:var(--color-text-muted)"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Under 60 min? Water + electrolytes are sufficient</div>
                    <div class="fuel-why">Glycogen stores handle most sub-60 min sessions, even at high intensity.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- POST -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">Within 30–60 min</span>
              <span class="timeline-phase-name">Recovery</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi mod"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Moderate-GI carbs + protein (3:1 ratio)</div>
                    <div class="fuel-why">Muscles are maximally insulin-sensitive after intense work. Glucose is preferentially stored as glycogen, not spiking blood sugar.</div>
                    <span class="fuel-example">e.g. Smoothie with banana, whey protein, oat milk</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Follow up with a balanced whole-food meal within 2 hrs</div>
                    <span class="fuel-example">e.g. Rice bowl with chicken, roasted vegetables</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="run-card-footer">
          <span class="footer-icon">💡</span>
          <p><strong>Blood sugar win:</strong> High-intensity work dramatically improves insulin sensitivity for 24–48 hours after the session. These workouts are your metabolic superpower — the post-workout window is the best time to eat carbs.</p>
        </div>
      </div>
    </section>

    <!-- ============================================================
         LONG RUN
         ============================================================ -->
    <section class="run-type" id="long">
      <div class="run-card">
        <div class="run-card-header long">
          <div class="run-card-title">
            <div class="run-icon long">🛤️</div>
            <div>
              <h3>Long Run</h3>
              <span>Endurance runs, progression longs, back-to-backs</span>
            </div>
          </div>
          <div class="run-meta">
            <span class="run-meta-tag">90+ min</span>
            <span class="run-meta-tag">Moderate intensity</span>
            <span class="run-meta-tag">Carb needs: High</span>
          </div>
        </div>

        <div class="timeline long">
          <!-- NIGHT BEFORE -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">Night before</span>
              <span class="timeline-phase-name">Carb Prime</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Carb-focused dinner — top off liver and muscle glycogen</div>
                    <div class="fuel-why">Low-GI whole-food carbs at dinner allow overnight glycogen saturation without a late-night glucose spike.</div>
                    <span class="fuel-example">e.g. Pasta with olive oil, grilled salmon, and roasted vegetables</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- PRE -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">2–3 hrs before</span>
              <span class="timeline-phase-name">Pre-Run</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Familiar low-GI breakfast — reliable, well-tested foods</div>
                    <div class="fuel-why">Sustained energy without the crash. Nothing new on long run day — gut comfort is critical.</div>
                    <span class="fuel-example">e.g. Oatmeal + banana + nut butter + coffee</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- DURING -->
          <div class="timeline-phase run-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">During</span>
              <span class="timeline-phase-name">The Run</span>
            </div>
            <div class="timeline-content">
              <div class="run-activity">
                <span class="run-activity-icon">🔵</span>
                90–150+ minutes
              </div>
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi high"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Begin fueling at 30–45 min, then every 20–30 min</div>
                    <div class="fuel-why">Start before you're depleted. Your muscles are burning glucose at high rates and absorbing it insulin-independently.</div>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi high"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Target 60–90 g carbs/hour using glucose + fructose blends</div>
                    <div class="fuel-why">Dual-transport (SGLT1 + GLUT5) maximizes absorption. Train the gut by practicing this in training, not on race day.</div>
                    <span class="fuel-example">e.g. Gels + sports drink, or chews + water</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low" style="background:var(--color-text-muted)"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Electrolytes + water throughout</div>
                    <div class="fuel-why">Sodium and fluid prevent hyponatremia and maintain performance.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- POST -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">Within 30 min</span>
              <span class="timeline-phase-name">Rapid Reload</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi high"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">High-GI carbs + protein immediately — don't delay</div>
                    <div class="fuel-why">Glycogen resynthesis rate is 2–3× faster in this window. Your muscles are sponges. This is the best possible time to eat fast carbs.</div>
                    <span class="fuel-example">e.g. Chocolate milk, recovery shake, white rice + eggs</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Full balanced meal within 2 hours</div>
                    <div class="fuel-why">Transition back to whole-food, fiber-rich eating for sustained recovery and blood sugar stability.</div>
                    <span class="fuel-example">e.g. Grain bowl with lean protein, roasted veggies, tahini</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="run-card-footer">
          <span class="footer-icon">💡</span>
          <p><strong>Blood sugar win:</strong> Long runs deplete glycogen significantly — your body <em>needs</em> carbs to recover. This is not the time to restrict. Eat the carbs, pair with protein, then return to controlled eating at dinner.</p>
        </div>
      </div>
    </section>

    <!-- ============================================================
         RACE DAY
         ============================================================ -->
    <section class="run-type" id="race">
      <div class="run-card">
        <div class="run-card-header race">
          <div class="run-card-title">
            <div class="run-icon race">🏆</div>
            <div>
              <h3>Race Day</h3>
              <span>Half marathon, marathon, ultras — max effort</span>
            </div>
          </div>
          <div class="run-meta">
            <span class="run-meta-tag">90 min – 5+ hrs</span>
            <span class="run-meta-tag">Race effort</span>
            <span class="run-meta-tag">Carb needs: Maximum</span>
          </div>
        </div>

        <div class="timeline race">
          <!-- 2-3 DAYS BEFORE -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">2–3 days before</span>
              <span class="timeline-phase-name">Carb Load</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Increase carb intake to 8–12 g/kg bodyweight per day</div>
                    <div class="fuel-why">Maximize muscle and liver glycogen stores. Use familiar, well-tolerated foods. Spread across meals to avoid large single-meal glucose loads.</div>
                    <span class="fuel-example">e.g. Extra rice, pasta, bread, potatoes at each meal + normal protein</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Reduce fiber slightly in the last 24 hrs</div>
                    <div class="fuel-why">Minimizes GI distress on race morning. Shift from brown rice to white rice, etc.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- RACE MORNING -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">3 hrs before start</span>
              <span class="timeline-phase-name">Race Morning</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Tried-and-true breakfast: low-GI, moderate portion</div>
                    <div class="fuel-why">Top off liver glycogen (which depletes overnight). Avoid anything high-fat or high-fiber — minimize gut risk.</div>
                    <span class="fuel-example">e.g. White toast + peanut butter + banana + coffee</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi mod"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Small top-up 15–30 min before gun: gel or sports drink</div>
                    <div class="fuel-why">Ensures blood glucose is primed as you start. The imminent exercise prevents an insulin overshoot.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- DURING -->
          <div class="timeline-phase run-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">During</span>
              <span class="timeline-phase-name">The Race</span>
            </div>
            <div class="timeline-content">
              <div class="run-activity">
                <span class="run-activity-icon">🟣</span>
                Race effort — execute your fueling plan
              </div>
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi high"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">60–90+ g carbs/hour — start at mile 3–4, not when you feel depleted</div>
                    <div class="fuel-why">By the time you feel the bonk, it's too late. Early, consistent fueling maintains blood glucose and spares glycogen.</div>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi high"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Use glucose:fructose blends (2:1 ratio) — practice in training</div>
                    <div class="fuel-why">Dual-transport maximizes absorption and reduces GI distress at high intake rates. Nothing new on race day.</div>
                    <span class="fuel-example">e.g. Gel every 25 min + sips of sports drink at aid stations</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low" style="background:var(--color-text-muted)"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Sodium: 500–1000 mg/hr depending on sweat rate</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- POST -->
          <div class="timeline-phase">
            <div class="timeline-label">
              <div class="timeline-dot"></div>
              <span class="timeline-time">Finish → 2 hrs</span>
              <span class="timeline-phase-name">Celebrate & Reload</span>
            </div>
            <div class="timeline-content">
              <div class="fuel-items">
                <div class="fuel-item">
                  <span class="fuel-gi high"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Immediate: whatever sounds good + protein</div>
                    <div class="fuel-why">Glycogen is severely depleted. Your muscles will aggressively absorb glucose. This is not the time for restriction — eat and recover.</div>
                    <span class="fuel-example">e.g. Post-race banana, bagel, chocolate milk, pizza later 🍕</span>
                  </div>
                </div>
                <div class="fuel-item">
                  <span class="fuel-gi low"></span>
                  <div class="fuel-text">
                    <div class="fuel-what">Return to balanced, whole-food eating by the next day</div>
                    <div class="fuel-why">The recovery window extends 24+ hours, but you can transition back to controlled eating once the immediate reload is done.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="run-card-footer">
          <span class="footer-icon">💡</span>
          <p><strong>Blood sugar win:</strong> Race day is about performance, full stop. Your muscles will handle massive carb loads during and after the effort. Trust the physiology — restrict on rest days, not race day.</p>
        </div>
      </div>
    </section>

    <!-- ============================================================
         WEEKLY CARB PERIODIZATION
         ============================================================ -->
    <section class="weekly-section" id="weekly">
      <div class="run-card weekly-card">
        <div class="weekly-card-header">
          <div class="run-icon" style="background:var(--color-text)">📅</div>
          <div>
            <h3>Your Training Week
              <span>Carb periodization: Wed intervals · Sat long run · 70 kg / 154 lb runner</span>
            </h3>
          </div>
        </div>

        <!-- BAR CHART -->
        <div class="carb-chart">
          <div class="carb-chart-label">Daily carbohydrate intake (grams) — scaled to a 70 kg runner</div>
          <div class="chart-container" id="carbChart">
            <!-- Rendered by JS -->
          </div>
        </div>

        <!-- DAY CARDS -->
        <div class="weekly-days">

          <!-- MONDAY -->
          <div class="day-card">
            <div class="day-card-day">Monday</div>
            <div class="day-card-type"><span class="day-card-type-dot" style="background:var(--color-easy)"></span> Easy Run</div>
            <div class="day-card-carb moderate">5–6 g/kg</div>
            <ul class="day-card-meals">
              <li><strong>Focus:</strong> Whole-food meals, normal portions</li>
              <li>Carbs paired with protein + fat at every meal</li>
              <li>Vegetables first, carbs second</li>
            </ul>
          </div>

          <!-- TUESDAY -->
          <div class="day-card prime-day">
            <div class="day-card-day">Tuesday</div>
            <div class="day-card-type"><span class="day-card-type-dot" style="background:var(--color-intervals);opacity:0.5"></span> Easy / Pre-load</div>
            <div class="day-card-carb moderate">6–7 g/kg</div>
            <ul class="day-card-meals">
              <li><strong>Nudge up:</strong> Extra serving of carbs at lunch + dinner</li>
              <li>Preparing glycogen for tomorrow's hard session</li>
              <li>Low-GI sources: sweet potato, oats, basmati rice</li>
            </ul>
          </div>

          <!-- WEDNESDAY -->
          <div class="day-card workout-day">
            <div class="day-card-day">Wednesday</div>
            <div class="day-card-type"><span class="day-card-type-dot" style="background:var(--color-intervals)"></span> Intervals</div>
            <div class="day-card-carb high">7–8 g/kg</div>
            <ul class="day-card-meals">
              <li><strong>Pre-run:</strong> Low-GI meal 2–3 hrs before</li>
              <li><strong>During:</strong> Sports drink if &gt;60 min</li>
              <li><strong>Post-run:</strong> Carbs + protein immediately — muscles are sponges</li>
              <li>Higher carbs across all meals today</li>
            </ul>
          </div>

          <!-- THURSDAY -->
          <div class="day-card">
            <div class="day-card-day">Thursday</div>
            <div class="day-card-type"><span class="day-card-type-dot" style="background:#d4d0c8"></span> Rest / Recovery</div>
            <div class="day-card-carb low">3–5 g/kg</div>
            <ul class="day-card-meals">
              <li><strong>Lowest carb day</strong> — lean into protein, vegetables, healthy fats</li>
              <li>Great day for veggie-first meals</li>
              <li>Blood sugar is easiest to manage today</li>
            </ul>
          </div>

          <!-- FRIDAY -->
          <div class="day-card prime-day">
            <div class="day-card-day">Friday</div>
            <div class="day-card-type"><span class="day-card-type-dot" style="background:var(--color-long);opacity:0.5"></span> Easy / Pre-load</div>
            <div class="day-card-carb highest">7–8 g/kg</div>
            <ul class="day-card-meals">
              <li><strong>This is the key day.</strong> Bump carbs up to prime glycogen for Saturday</li>
              <li>Add carbs to existing meals — don't create one huge pasta dinner</li>
              <li>Extra toast at breakfast, larger rice portion at lunch, carb-forward dinner</li>
              <li>Walk 15 min after meals to blunt spikes</li>
            </ul>
          </div>

          <!-- SATURDAY -->
          <div class="day-card workout-day">
            <div class="day-card-day">Saturday</div>
            <div class="day-card-type"><span class="day-card-type-dot" style="background:var(--color-long)"></span> Long Run</div>
            <div class="day-card-carb highest">8–10 g/kg</div>
            <ul class="day-card-meals">
              <li><strong>Pre-run:</strong> Familiar low-GI breakfast 2–3 hrs before</li>
              <li><strong>During:</strong> 60–90 g/hr gels + drink starting at 30–45 min</li>
              <li><strong>Post-run:</strong> Fast carbs + protein within 30 min</li>
              <li>Highest carb day — justified by the glycogen debt</li>
            </ul>
          </div>

          <!-- SUNDAY -->
          <div class="day-card">
            <div class="day-card-day">Sunday</div>
            <div class="day-card-type"><span class="day-card-type-dot" style="background:var(--color-easy);opacity:0.5"></span> Recovery</div>
            <div class="day-card-carb moderate">5–6 g/kg</div>
            <ul class="day-card-meals">
              <li><strong>Moderate carbs</strong> — still restocking glycogen from Saturday</li>
              <li>Return to whole-food, fiber-rich meals</li>
              <li>Pair carbs with protein + fat, eat controlled portions</li>
            </ul>
          </div>

        </div>

        <!-- CALLOUTS -->
        <div class="weekly-callout">
          <div class="weekly-callout-item">
            <span class="footer-icon">⚠️</span>
            <p><strong>Friday is your blood sugar tension point.</strong> You're increasing carbs ~30–40% above baseline while not doing a hard workout. Mitigate this by: spreading carbs across 5–6 smaller meals, using low-GI sources (sweet potato, oats, basmati rice instead of white bread), always pairing with protein, and walking 15 minutes after each meal.</p>
          </div>
          <div class="weekly-callout-item">
            <span class="footer-icon">💡</span>
            <p><strong>This is not race-week loading.</strong> You're going from ~350g to ~500g for a 70 kg runner — roughly one extra cup of rice per meal. Your glycogen stores have room because you trained Monday through Wednesday. The body handles this much better than race-week loading where you've tapered.</p>
          </div>
          <div class="weekly-callout-item">
            <span class="footer-icon">📊</span>
            <p><strong>Thursday is your metabolic reset.</strong> Rest day + lowest carbs = the most blood-sugar-friendly day of the week. This is where you "earn back" the controlled eating that makes Friday and Saturday's higher carbs a net-neutral for your weekly glucose average.</p>
          </div>
        </div>

      </div>
    </section>

    <!-- ============================================================
         CONTEXT CARDS: REST-OF-DAY
         ============================================================ -->
    <section class="context-section">
      <div class="section-header">
        <h2>The Rest of the Day</h2>
        <p>Away from workouts, these habits keep blood sugar stable without compromising your training.</p>
      </div>

      <div class="context-grid">
        <div class="context-card">
          <div class="context-card-icon">🥗</div>
          <h3>Veggie-First Meal Order</h3>
          <p>Eat vegetables and protein before carbs in a meal. Clinical studies show this simple reordering can reduce post-meal glucose spikes by 30–40%.</p>
        </div>
        <div class="context-card">
          <div class="context-card-icon">🫘</div>
          <h3>Pair, Don't Bare</h3>
          <p>Never eat carbs alone. Always combine with protein, healthy fat, or fiber. The combination slows gastric emptying and glucose absorption.</p>
        </div>
        <div class="context-card">
          <div class="context-card-icon">🚶</div>
          <h3>Post-Meal Movement</h3>
          <p>A 10–15 minute walk after meals significantly lowers glucose excursions. Even gentle movement activates muscle glucose uptake.</p>
        </div>
        <div class="context-card">
          <div class="context-card-icon">📊</div>
          <h3>Consider a CGM</h3>
          <p>A continuous glucose monitor for 2–4 weeks reveals your personal responses. You'll learn which foods spike you and how different runs affect your glucose.</p>
        </div>
        <div class="context-card">
          <div class="context-card-icon">🌾</div>
          <h3>Choose Intact Grains</h3>
          <p>Steel-cut oats over instant. Brown rice over white (except post-run). Whole fruit over juice. The fiber matrix slows absorption dramatically.</p>
        </div>
        <div class="context-card">
          <div class="context-card-icon">📅</div>
          <h3>Periodize Your Carbs</h3>
          <p>Match carb intake to training load. High-carb on hard days, moderate on easy days, lower on rest days. Don't eat like it's race week every day.</p>
        </div>
      </div>
    </section>

    <!-- ======== FOOTER ======== -->
    <footer class="page-footer">
      <p>This guide is for informational purposes based on published sports nutrition research. It is not medical advice. If you have a metabolic condition, please work with a sports dietitian and your healthcare provider.</p>
    </footer>

  </div>

  <script>
    // ============================
    // Weekly carb chart
    // ============================
    const chartData = [
      { day: 'Mon', label: 'Easy', grams: '350–420', pct: 42, cls: 'easy-bar' },
      { day: 'Tue', label: 'Pre-load', grams: '420–490', pct: 52, cls: 'prime-bar' },
      { day: 'Wed', label: 'Intervals', grams: '490–560', pct: 65, cls: 'intervals-bar' },
      { day: 'Thu', label: 'Rest', grams: '210–350', pct: 28, cls: 'rest' },
      { day: 'Fri', label: 'Pre-load', grams: '490–560', pct: 65, cls: 'prime-bar' },
      { day: 'Sat', label: 'Long Run', grams: '560–700', pct: 85, cls: 'long-bar' },
      { day: 'Sun', label: 'Recovery', grams: '350–420', pct: 42, cls: 'recovery-bar' },
    ];

    const chart = document.getElementById('carbChart');
    if (chart) {
      chartData.forEach(d => {
        const col = document.createElement('div');
        col.className = 'chart-col';
        const isWorkout = d.day === 'Wed' || d.day === 'Sat';
        col.innerHTML = `
          <div class="chart-bar-wrapper">
            <div class="chart-bar ${d.cls}" style="height: 0%" data-height="${d.pct}">
              <span class="chart-bar-value">${d.grams}g</span>
            </div>
          </div>
          <span class="chart-day-label ${isWorkout ? 'has-workout' : ''}">${d.day}</span>
        `;
        chart.appendChild(col);
      });

      // Animate bars on scroll
      const chartObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            const bars = entry.target.querySelectorAll('.chart-bar');
            bars.forEach((bar, i) => {
              setTimeout(() => {
                bar.style.height = bar.dataset.height + '%';
              }, i * 80);
            });
            chartObserver.unobserve(entry.target);
          }
        });
      }, { threshold: 0.3 });
      chartObserver.observe(chart);
    }

    // ============================
    // Scroll-triggered reveal animation
    // ============================
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.08 });

    document.querySelectorAll('.run-type').forEach(el => observer.observe(el));

    // ============================
    // Active nav pill tracking
    // ============================
    const allSections = document.querySelectorAll('.run-type, .weekly-section');
    const pills = document.querySelectorAll('.nav-pill');

    const navObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          pills.forEach(p => p.classList.remove('active'));
          const id = entry.target.id;
          const activePill = document.querySelector(`.nav-pill[href="#${id}"]`);
          if (activePill) activePill.classList.add('active');
        }
      });
    }, { threshold: 0.2, rootMargin: '-80px 0px -40% 0px' });

    allSections.forEach(s => navObserver.observe(s));

    // ============================
    // Smooth scroll for nav pills
    // ============================
    pills.forEach(pill => {
      pill.addEventListener('click', (e) => {
        e.preventDefault();
        const target = document.querySelector(pill.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
      });
    });
  </script>

</body>
</html>
