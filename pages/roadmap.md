---
layout: page
title: KiaWriteBot Roadmap
permalink: /
---

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="title" content="{{ page.title | escape }}" />
  <meta name="description" content="A detailed public roadmap for KiaWriteBot — a versatile Telegram bot." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="{{ site.url }}{{ site.baseurl }}" />
  <meta property="og:title" content="{{ page.title | escape }}" />
  <meta property="og:image" content="https://hosseinskia.github.io/kiawritebot-roadmap/images/kiawritebot.png" />
  <meta name="google-site-verification" content="jh4M3O9h4h6N0abGGjbzdi09_MbPktaRKi7lnvAa3s8" />
  <link rel="shortcut icon" type="image/png" href="https://cdn-icons-png.flaticon.com/512/7402/7402503.png">
  <title>{{ page.title }}</title>
</head>

<style>

  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wght@0,100..900;1,100..900&display=swap');

  html {
    scroll-behavior: smooth;
  }
  body {
    font-family: 'Noto Sans', Arial, sans-serif !important;
    line-height: 1.6;
    color: #333;
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
    background: #f9f9f9;
  }
  h1, h2, h3 {
    color: #2c3e50;
    border-bottom: 2px solid #3498db;
    padding-bottom: 8px;
    margin-top: 1.5em;
  }
  h1 {
    font-size: 2.5em;
    text-align: center;
    margin-bottom: 0.5em;
    animation: fadeIn 1s ease;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(-10px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .copyright {
    text-align: center;
    font-size: 14px;
    color: #555;
    padding: 20px 0;
    border-top: 1px solid #e0e0e0;
    background-color: #f3f4f6;
    user-select: none;
    transition: color 0.3s ease;
  }
  
  .copyright a {
    color: #3498db;
    text-decoration: none;
    font-weight: 600;
  }
  
  .copyright a:hover,
  .copyright a:focus {
    text-decoration: underline;
    color: #1d4ed8;
  }

  .about-content {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    flex-wrap: wrap;
  }
  
  
  .about-text {
    flex: 1;
    min-width: 250px;
  }
  
  .about-image {
    max-width: 18rem;
    height: auto;
    border-radius: 8px;
    margin: auto;
  }

  .toc {
    background: #f9fafb;
    border: 1px solid #e5e7eb;
    border-radius: 10px;
    padding: 20px 25px;
    margin-bottom: 30px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
  }
  
  .toc ul {
    list-style: none;
    padding-left: 0;
    margin: 0;
  }
  
  .toc li {
    margin: 10px 0;
    font-size: 16px;
    transition: all 0.2s ease-in-out;
  }
  
  .toc a {
    color: #1d4ed8;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.2s;
  }
  
  .toc a:hover {
    color: #2563eb;
    text-decoration: underline;
  }

  .toc ul {
    list-style: none;
    padding: 0;
  }
  .toc li {
    margin: 8px 0;
  }
  .toc a {
    color: #3498db;
    text-decoration: none;
  }
  .toc a:hover {
    text-decoration: underline;
  }
  details {
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
    margin: 10px 0;
    padding: 10px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    overflow: hidden;
  }
  
  details:hover {
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
  }
  
  details[open] > *:not(summary) {
    animation: slideFade 0.3s ease;
  }
  
  @keyframes slideFade {
    from {
      opacity: 0;
      transform: translateY(-5px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  summary {
    font-weight: bold;
    cursor: pointer;
    color: #2c3e50;
    padding: 10px;
    background: #ecf0f1;
    border-radius: 4px;
  }
  summary:hover {
    background: #dfe6e9;
  }
  li {
    margin: 8px 0;
  }
  li:hover {
  color: #005fa3;
  }
  .completed::before {
    content: '✅ ';
    color: #27ae60;
  }
  .progress::before {
    content: '⏳ ';
    color: #e67e22;
  }
  .about {
    background: #fff;
    border-left: 4px solid #3498db;
    padding: 15px;
    margin-bottom: 20px;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  .topics {
    margin-top: 10px;
  }
  .topics span {
    font-weight: 900;
    display: inline-block;
    background: #3498db;
    color: #fff;
    padding: 5px 10px;
    margin: 5px 5px 0 0;
    border-radius: 12px;
    font-size: 0.9em;
  }
  
  .command-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
  padding: 15px 0 0 0;
}

.command-card {
  background: #fff;
  border-radius: 8px;
  padding: 15px 20px;
  box-shadow: 0 2px 8px rgb(0 0 0 / 0.1);
  transition: box-shadow 0.3s ease;
  cursor: default;
}

.command-card:hover {
  box-shadow: 0 6px 15px rgb(0 0 0 / 0.15);
}

.command-card h4 {
  margin-top: 0;
  font-size: 1.1rem;
  color: #222;
}

.command-card code {
  background-color: #f3f4f6;
  padding: 3px 6px;
  border-radius: 4px;
  font-family: Consolas, monospace;
  font-weight: 600;
}

.command-card p {
  margin: 8px 0 0 0;
  font-size: 0.9rem;
  color: #444;
  line-height: 1.3;
}

  @media (max-width: 600px) {
    body {
      padding: 10px;
    }
    h1 {
      font-size: 2em;
    }
    .command-grid {
      grid-template-columns: 1fr;
    }
    .about-image{
        max-width: 100%;
    }
  }

  .command-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
  padding: 15px 0 0 0;
}

</style>

# KiaWriteBot Roadmap

Welcome to the public development roadmap for **KiaWriteBot**, a feature-rich Telegram bot designed to enhance user interactions with tools for news, weather, coding, and more. Explore our progress, planned features, and contribute to shaping the future of KiaWriteBot.

<div class="about">
  <div class="about-content">
    <img src="{{ site.baseurl }}/images/kiawritebot.png" onerror="this.onerror=null; this.src='/images/kiawritebot.png';" loading="lazy" alt="KiaWriteBot Logo" class="about-image" />
    <div class="about-text">
      <strong>About KiaWriteBot</strong><br>
      KiaWriteBot is a feature-packed Telegram bot offering news, weather, QR code generation, YouTube downloads, and more. Built with Node.js, Python, MongoDB, and Upstash Redis, it ensures secure, scalable interactions with a robust admin dashboard.
      <div class="topics">
        <span>telegram-bot</span>
        <span>nodejs</span>
        <span>mongodb</span>
        <span>redis</span>
        <span>telegraf</span>
        <span>python</span>
        <span>express</span>
        <span>mongoose</span>
        <span>rate-limiting</span>
        <span>webhook</span>
        <span>security</span>
        <span>api</span>
        <span>openweathermap</span>
        <span>newsapi</span>
        <span>youtube-dl</span>
        <span>qr-code</span>
        <span>translation</span>
        <span>polls</span>
        <span>admin-dashboard</span>
        <span>real-time</span>
      </div>
    </div>
  </div>
</div>

## Table of Contents

<div class="toc">
  <ul>
    <li><a href="#feature-additions">Feature Additions</a></li>
    <li><a href="#security-improvements">Security Improvements</a></li>
    <li><a href="#performance--deployment">Performance & Deployment</a></li>
    <li><a href="#analytics-and-monitoring">Analytics and Monitoring</a></li>
    <li><a href="#admin-panel-features">Admin Panel Features</a></li>
    <li><a href="#user-experience">User Experience</a></li>
    <li><a href="#uxui-improvements">UX/UI Improvements</a></li>
    <li><a href="#telegram-bot-command-ideas">Telegram Bot Command Ideas</a></li>
  </ul>
</div>

## Feature Additions

<details>
  <summary>New Commands and Functionalities</summary>
  <ul>
    <li class="progress">Add <code>/github</code> command with full GitHub API integration (repos, user info, issues, PRs, commits, orgs, gists).</li>
    <li class="progress">Implement <code>/siteinfo</code> command (domain info, SSL status, server details, uptime, traffic stats, technologies used).</li>
    <li class="completed">Create <code>/weather</code> command for detailed weather info (current, forecast, alerts, historical).</li>
    <li class="completed">Build <code>/translate</code> command using translation APIs (multi-language, auto-detect, text-to-speech).</li>
    <li class="completed">Develop <code>/news</code> command for latest headlines by category and region.</li>
    <li>Add <code>/crypto</code> command for real-time cryptocurrency prices, market caps, trends.</li>
    <li>Add <code>/stock</code> command for stock prices, charts, company info.</li>
    <li class="completed">Add <code>/define</code> command for dictionary and thesaurus lookup with examples.</li>
    <li class="completed">Build <code>/currency</code> command for live currency conversion and historical rates.</li>
    <li class="completed">Add <code>/joke</code> command for random jokes by category or type.</li>
    <li>Add <code>/movie</code> command for movie info, ratings, trailers, actors via IMDB.</li>
    <li>Add <code>/randomfact</code> for random tech/programming facts.</li>
    <li>Add <code>/regex &lt;pattern&gt; &lt;text&gt;</code> to test regex patterns and show matches.</li>
    <li>Add <code>/emoji &lt;keyword&gt;</code> to search for emojis by keyword.</li>
    <li>Add <code>/md5 &lt;text&gt;</code> to return MD5 hash of input text.</li>
    <li>Add <code>/shorturl &lt;url&gt;</code> to create shortened URLs via popular shorteners.</li>
    <li>Add <code>/ascii &lt;text&gt;</code> to convert text to ASCII art.</li>
  </ul>
</details>

## Security Improvements

<details>
  <summary>Enhancing System Security</summary>
  <ul>
    <li>Replace cookie-based sessions with JWT (JSON Web Token).</li>
    <li>Strengthen API and admin panel security for unverified users.</li>
    <li>Optional: Replace key-based logging with basic authentication.</li>
    <li>Implement Role-Based Access Control (RBAC) for fine-grained permissions.</li>
    <li>Log sessions in admin panel’s Dash Security page (create <code>adminsSessions</code> collection).</li>
    <li>Set up error tracking with tools like Sentry or LogRocket.</li>
  </ul>
</details>

## Performance & Deployment

<details>
  <summary>Optimizing Speed and Scalability</summary>
  <ul>
    <li>Improve admin panel performance (investigate Vercel latency).</li>
    <li>Deploy to a faster service provider for better reliability.</li>
    <li>Auto-archive old logs and analytics for performance optimization.</li>
  </ul>
</details>

## Analytics and Monitoring

<details>
  <summary>Advanced Data Insights</summary>
  <ul>
    <li>Create feature to calculate and save user messages and stats (daily/weekly/monthly).</li>
    <li>Store analytics in a new collection, display on an analytics history page.</li>
    <li>Add health monitoring metrics: uptime, errors, response times.</li>
    <li>Enable scheduled report generation for analytics.</li>
    <li>Build custom report builder for flexible metrics.</li>
    <li>Integrate predictive analytics for usage trends.</li>
    <li>Automate trend analysis reports.</li>
    <li>Create live dashboard with real-time stats.</li>
  </ul>
</details>

## Admin Panel Features

<details>
  <summary>Enhancing Admin Capabilities</summary>
  <ul>
    <li class="completed">Fix metadata on every page.</li>
    <li>Add Notification database model for tracking alerts.</li>
    <li class="completed">Create log page to save and display logs in admin panel.</li>
    <li>Enable scheduled posts system.</li>
    <li>Add command customization page.</li>
    <li>Allow toggling bot commands on/off.</li>
    <li>Implement moderation alerts for spam/harmful content.</li>
    <li>Enable export of analytics/logs in CSV or PDF.</li>
    <li>Add message filter settings (bad words, spam thresholds).</li>
  </ul>
</details>

## User Experience

<details>
  <summary>Improving User Interaction</summary>
  <ul>
    <li>Add interactive tutorials and onboarding for new users.</li>
    <li>Introduce collaboration tools: commenting on analytics, shared workspaces.</li>
    <li>Implement live support & ticketing system.</li>
  </ul>
</details>

## UX/UI Improvements

<details>
  <summary>Polishing the Interface</summary>
  <ul>
    <li>Add dark mode toggle for admin panel.</li>
    <li>Create customizable dashboard widgets for each admin.</li>
    <li>Add keyboard shortcuts for frequent admin actions.</li>
    <li>Improve mobile responsiveness of the admin panel.</li>
  </ul>
</details>

## Telegram Bot Command Ideas

<details open>
  <summary>100 Innovative Commands</summary>
  <div class="command-grid">
    <div class="command-card"><h4><code>/start</code></h4><p>Start interacting with the bot and see help info.</p></div>
    <div class="command-card"><h4><code>/help</code></h4><p>Show a list of available commands and usage tips.</p></div>
    <div class="command-card"><h4><code>/github</code></h4><p>Get GitHub user or repo info like stars, commits, issues.</p></div>
    <div class="command-card"><h4><code>/docker</code></h4><p>Fetch Docker Hub image stats and tags.</p></div>
    <div class="command-card"><h4><code>/npm</code></h4><p>Get details and stats about an NPM package.</p></div>
    <div class="command-card"><h4><code>/stackoverflow</code></h4><p>Search Stack Overflow questions and answers.</p></div>
    <div class="command-card"><h4><code>/wiki</code></h4><p>Summarize a Wikipedia article on a given topic.</p></div>
    <div class="command-card"><h4><code>/weather</code></h4><p>Get current weather info for any city.</p></div>
    <div class="command-card"><h4><code>/crypto</code></h4><p>Show latest cryptocurrency prices and market data.</p></div>
    <div class="command-card"><h4><code>/stock</code></h4><p>Fetch stock prices and charts for a given symbol.</p></div>
    <div class="command-card"><h4><code>/translate</code></h4><p>Translate text into a specified language.</p></div>
    <div class="command-card"><h4><code>/joke</code></h4><p>Get a random programming or tech joke.</p></div>
    <div class="command-card"><h4><code>/quote</code></h4><p>Receive an inspirational tech or programming quote.</p></div>
    <div class="command-card"><h4><code>/fortune</code></h4><p>Get a witty fortune cookie message.</p></div>
    <div class="command-card"><h4><code>/ascii</code></h4><p>Convert text to ASCII art.</p></div>
    <div class="command-card"><h4><code>/time</code></h4><p>Show current time in any timezone or city.</p></div>
    <div class="command-card"><h4><code>/randomuser</code></h4><p>Generate a random user profile with name and avatar.</p></div>
    <div class="command-card"><h4><code>/ipinfo</code></h4><p>Retrieve geolocation info for an IP address.</p></div>
    <div class="command-card"><h4><code>/qr</code></h4><p>Generate a QR code image from text or URL.</p></div>
    <div class="command-card"><h4><code>/md5</code></h4><p>Calculate MD5 hash of input text.</p></div>
    <div class="command-card"><h4><code>/shorturl</code></h4><p>Shorten URLs using popular URL shorteners.</p></div>
    <div class="command-card"><h4><code>/color</code></h4><p>Display color info and preview for a hex code or name.</p></div>
    <div class="command-card"><h4><code>/emoji</code></h4><p>Search and display emojis by keyword.</p></div>
    <div class="command-card"><h4><code>/regex</code></h4><p>Test a regex pattern against provided text.</p></div>
    <div class="command-card"><h4><code>/bug</code></h4><p>Create or list GitHub issues in a repo.</p></div>
    <div class="command-card"><h4><code>/ci-status</code></h4><p>Check latest CI/CD pipeline status for a repo.</p></div>
    <div class="command-card"><h4><code>/dockerfile</code></h4><p>Analyze Dockerfile and give optimization tips.</p></div>
    <div class="command-card"><h4><code>/k8s</code></h4><p>Show Kubernetes pod, deployment, and service info.</p></div>
    <div class="command-card"><h4><code>/aws</code></h4><p>Get AWS resource info and billing estimates.</p></div>
    <div class="command-card"><h4><code>/git</code></h4><p>Perform Git commands summary like status or log.</p></div>
    <div class="command-card"><h4><code>/lint</code></h4><p>Run lint checks on code snippets.</p></div>
    <div class="command-card"><h4><code>/format</code></h4><p>Format code in various programming languages.</p></div>
    <div class="command-card"><h4><code>/movie</code></h4><p>Search movies and get info, ratings, trailers.</p></div>
    <div class="command-card"><h4><code>/book</code></h4><p>Search books info by title or author.</p></div>
    <div class="command-card"><h4><code>/news</code></h4><p>Fetch latest headlines by category or region.</p></div>
    <div class="command-card"><h4><code>/poll</code></h4><p>Create and manage polls in chat.</p></div>
    <div class="command-card"><h4><code>/reminder</code></h4><p>Set reminders for important tasks.</p></div>
    <div class="command-card"><h4><code>/todo</code></h4><p>Manage a personal to-do list.</p></div>
    <div class="command-card"><h4><code>/currency</code></h4><p>Convert currencies with live exchange rates.</p></div>
    <div class="command-card"><h4><code>/convert</code></h4><p>Unit conversion (length, weight, temperature).</p></div>
    <div class="command-card"><h4><code>/barcode</code></h4><p>Generate barcode images from text.</p></div>
    <div class="command-card"><h4><code>/pdf</code></h4><p>Convert text or URLs to PDF files.</p></div>
    <div class="command-card"><h4><code>/urlinfo</code></h4><p>Fetch metadata (title, description, image) from a URL.</p></div>
    <div class="command-card"><h4><code>/weatherforecast</code></h4><p>Get weather forecast for next days.</p></div>
    <div class="command-card"><h4><code>/calorie</code></h4><p>Lookup calorie info for food items.</p></div>
    <div class="command-card"><h4><code>/covid</code></h4><p>Show latest COVID-19 stats by country.</p></div>
    <div class="command-card"><h4><code>/bitcoin</code></h4><p>Get Bitcoin price and market data.</p></div>
    <div class="command-card"><h4><code>/ethereum</code></h4><p>Get Ethereum price and market data.</p></div>
    <div class="command-card"><h4><code>/youtube</code></h4><p>Search YouTube videos and get info.</p></div>
    <div class="command-card"><h4><code>/spotify</code></h4><p>Search Spotify tracks, albums, artists.</p></div>
    <div class="command-card"><h4><code>/lyrics</code></h4><p>Find song lyrics by title or artist.</p></div>
    <div class="command-card"><h4><code>/dictionary</code></h4><p>Define words with examples and synonyms.</p></div>
    <div class="command-card"><h4><code>/thesaurus</code></h4><p>Find synonyms and antonyms.</p></div>
    <div class="command-card"><h4><code>/calendar</code></h4><p>Show calendar for a given month/year.</p></div>
    <div class="command-card"><h4><code>/quoteoftheday</code></h4><p>Get a daily inspirational quote.</p></div>
    <div class="command-card"><h4><code>/fact</code></h4><p>Share a random tech or programming fact.</p></div>
    <div class="command-card"><h4><code>/weatheralerts</code></h4><p>Get severe weather alerts for locations.</p></div>
    <div class="command-card"><h4><code>/stocknews</code></h4><p>Latest news related to a stock symbol.</p></div>
    <div class="command-card"><h4><code>/vpn</code></h4><p>Provide info or tips about VPNs.</p></div>
    <div class="command-card"><h4><code>/proxy</code></h4><p>Fetch free proxy lists or check proxy status.</p></div>
    <div class="command-card"><h4><code>/iplookup</code></h4><p>Detailed info on any IP address.</p></div>
    <div class="command-card"><h4><code>/speedtest</code></h4><p>Run an internet speed test and show results.</p></div>
    <div class="command-card"><h4><code>/dnslookup</code></h4><p>Perform DNS queries for a domain.</p></div>
    <div class="command-card"><h4><code>/whois</code></h4><p>Whois info for domains or IPs.</p></div>
    <div class="command-card"><h4><code>/hostname</code></h4><p>Resolve hostname to IP or vice versa.</p></div>
    <div class="command-card"><h4><code>/technews</code></h4><p>Latest news on technology and gadgets.</p></div>
    <div class="command-card"><h4><code>/programmingtips</code></h4><p>Share random programming tips or tricks.</p></div>
    <div class="command-card"><h4><code>/stackexchange</code></h4><p>Search questions on Stack Exchange network.</p></div>
    <div class="command-card"><h4><code>/devtools</code></h4><p>Show list of popular dev tools and resources.</p></div>
    <div class="command-card"><h4><code>/shell</code></h4><p>Execute shell commands (sandboxed).</p></div>
    <div class="command-card"><h4><code>/curl</code></h4><p>Make HTTP GET/POST requests and show responses.</p></div>
    <div class="command-card"><h4><code>/json</code></h4><p>Validate or prettify JSON text.</p></div>
    <div class="command-card"><h4><code>/yaml</code></h4><p>Validate or prettify YAML text.</p></div>
    <div class="command-card"><h4><code>/xml</code></h4><p>Validate or prettify XML content.</p></div>
    <div class="command-card"><h4><code>/base64</code></h4><p>Encode or decode base64 strings.</p></div>
    <div class="command-card"><h4><code>/uuid</code></h4><p>Generate a new UUID.</p></div>
    <div class="command-card"><h4><code>/passwordgen</code></h4><p>Generate secure random passwords.</p></div>
    <div class="command-card"><h4><code>/reminderlist</code></h4><p>List all your reminders.</p></div>
    <div class="command-card"><h4><code>/gitstats</code></h4><p>Show stats of GitHub repo commits/contributors.</p></div>
    <div class="command-card"><h4><code>/markdown</code></h4><p>Preview Markdown formatted text.</p></div>
    <div class="command-card"><h4><code>/html</code></h4><p>Render HTML snippet preview.</p></div>
    <div class="command-card"><h4><code>/css</code></h4><p>Provide CSS snippet or tips.</p></div>
    <div class="command-card"><h4><code>/js</code></h4><p>Run JavaScript snippet sandboxed.</p></div>
    <div class="command-card"><h4><code>/regexhelp</code></h4><p>Provide regex syntax help and examples.</p></div>
    <div class="command-card"><h4><code>/apihelp</code></h4><p>List popular APIs and how to use them.</p></div>
    <div class="command-card"><h4><code>/botinfo</code></h4><p>Show bot version and developer info.</p></div>
    <div class="command-card"><h4><code>/uptime</code></h4><p>Show how long the bot has been running.</p></div>
    <div class="command-card"><h4><code>/serverstatus</code></h4><p>Check status of a given server or service.</p></div>
    <div class="command-card"><h4><code>/ipblacklist</code></h4><p>Check if IP is blacklisted.</p></div>
    <div class="command-card"><h4><code>/devquotes</code></h4><p>Daily quotes from famous developers.</p></div>
    <div class="command-card"><h4><code>/frameworks</code></h4><p>List popular programming frameworks.</p></div>
    <div class="command-card"><h4><code>/libraries</code></h4><p>List useful programming libraries by language.</p></div>
    <div class="command-card"><h4><code>/chatgpt</code></h4><p>Use GPT API to answer any question.</p></div>
    <div class="command-card"><h4><code>/debug</code></h4><p>Help debug code or errors.</p></div>
    <div class="command-card"><h4><code>/devjobs</code></h4><p>Show latest developer job listings.</p></div>
    <div class="command-card"><h4><code>/gitclone</code></h4><p>Provide git clone command for repos.</p></div>
    <div class="command-card"><h4><code>/regexmatch</code></h4><p>Check if text matches a regex pattern.</p></div>
    <div class="command-card"><h4><code>/techevents</code></h4><p>List upcoming tech conferences and meetups.</p></div>
    <div class="command-card"><h4><code>/opensource</code></h4><p>Share popular open source projects.</p></div>
    <div class="command-card"><h4><code>/feedback</code></h4><p>Submit feedback or bug reports for the bot.</p></div>

  </div>
</details>

<footer class="copyright">
  &copy; <span id="year"></span> KiaWriteBot by 
  <a href="https://github.com/hosseinskia" target="_blank" rel="noopener noreferrer">hosseinskia</a>. All rights reserved.
</footer>

<script>
  document.addEventListener("DOMContentLoaded", () => {
    // Intercept TOC links
    document.querySelectorAll('.toc a').forEach(link => {
      link.addEventListener('click', e => {
        // Extract the anchor without #
        const targetId = link.getAttribute('href').slice(1);
        const targetEl = document.getElementById(targetId);

        if (targetEl) {
          const details = targetEl.nextElementSibling;
          if (details && details.tagName.toLowerCase() === 'details') {
            details.setAttribute('open', '');
          }
        }
      });
    });
  });
  document.getElementById('year').textContent = new Date().getFullYear();
</script>
