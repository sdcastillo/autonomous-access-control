---
layout: default
title: Autonomous Access Control
description: Synthetic camera events for security data and AI alarm access control systems.
samwiki: true
---

<p class="sw-level sw-level-beginner">
  <span class="sw-level-idx">Level 1</span>
  <span class="sw-level-name">Beginner</span>
</p>

<section class="sw-lede" aria-labelledby="about-title">
  <div class="sw-lede-copy">
    <h2 id="about-title">Camera events for alarm and access control</h2>
    <p>This repository is for security data and AI alarm access control systems. It holds one synthetic camera-event table, 200 rows dated from 1 January 2025 through 14 April 2025. The same rows are in <a href="https://github.com/sdcastillo/autonomous-access-control/blob/main/Synthetic_Camera_Event_Dataset.csv"><code>Synthetic_Camera_Event_Dataset.csv</code></a> and in the workbook <a href="https://github.com/sdcastillo/autonomous-access-control/blob/main/Security_Camera_Event_Dataset.xlsx"><code>Security_Camera_Event_Dataset.xlsx</code></a>. The note in <a href="https://github.com/sdcastillo/autonomous-access-control/blob/main/chatGPT%20prompt.md"><code>chatGPT prompt.md</code></a> says the rows are simulated with <a href="https://faker.readthedocs.io/">Faker</a>, a Python library for realistic fake data.</p>
    <p>Each row is one detection. The columns are UUID, cameraID, event Type, datetime, probability, model, video location, video index timestamp, and SiteID. Ten cameras, <code>CAM-001</code> through <code>CAM-010</code>, are spread across five sites, <code>SITE-01</code> through <code>SITE-05</code>. The event types are motion (60), face_recognized (48), vehicle_detected (47), and person_detected (45). The model field is EfficientDet (58), FasterRCNN (52), YOLOv8 (46), or YOLOv5 (44). Probabilities run from 0.50 to 0.99. A video path looks like <code>/videos/CAM-005/20250321_022734.mp4</code>, and the index timestamp on that row is <code>2:27:34</code>.</p>
    <p>The workbook keeps those rows on the sheet <code>Camera_Event_Dataset</code> and adds two summaries. <code>ISC Camera Scores</code> sums the probability column by camera and event type. <code>ISC Detections by Type of Event and Location 2025</code> splits the same scores by model, site, and month. The chart text in the file names motion detection, persons, vehicles, cameras, and risk. Pivot fields include the nine data columns plus day and month of the datetime.</p>
    <p><strong>Difficulty: beginner.</strong> On the SamWiki ladder this is Level 1, beginner. The work in the repository is reading a finished table and the short note on how to simulate one. Opening the CSV, filtering a camera or a site, and reading a probability is enough to see the shape of a log an alarm or access-control rule could score. The recreation guide that ships with the files is the Faker feature list in <code>chatGPT prompt.md</code>, repeated below: realistic fake values for databases, tests, and anonymized data, including names, addresses, emails, phone numbers, and dates, with locales and custom providers.</p>
  </div>
  <aside class="sw-find" aria-labelledby="facts-title">
    <h2 id="facts-title">On this page</h2>
    <ul>
      <li><strong>What it is</strong> Security data for AI alarm access control: 200 synthetic camera events in a CSV and an Excel workbook.</li>
      <li><strong>Who it is for</strong> Someone learning the columns of a camera-event log before writing an alarm or access rule.</li>
      <li><strong>Difficulty: beginner</strong> Level 1 on the SamWiki ladder. A spreadsheet and the Faker note.</li>
      <li><strong>In the table</strong> Four event types, four detector names, ten cameras, five sites, probabilities from 0.50 to 0.99.</li>
      <li><strong>How the rows were made</strong> Simulated with Faker, as written in <code>chatGPT prompt.md</code>.</li>
    </ul>
  </aside>
</section>

## How to recreate the synthetic datasets

- Generates various data types: names, addresses, emails, phone numbers, dates, and more.
- Supports multiple locales for internationalization.
- Allows customization through providers for specific data types.

## Contribute

A clearer note on a column, a correction to the camera-score reading, or a small example that uses these rows can come back as a pull request on this repository.

<div class="sw-actions">
  <a class="sw-btn sw-btn-source" href="https://github.com/sdcastillo/autonomous-access-control">View on GitHub</a>
  <a class="sw-btn sw-btn-pr" href="https://github.com/sdcastillo/autonomous-access-control/compare" target="_blank" rel="noopener noreferrer">Contribute / Open a PR</a>
</div>
