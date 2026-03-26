---
title: "Education Projects"
permalink: /education/
---

<style>
  .education-project-list {
    display: grid;
    gap: 2rem;
    margin-top: 2rem;
  }

  .education-project-card {
    display: grid;
    gap: 1.5rem;
    grid-template-columns: minmax(0, 320px) minmax(0, 1fr);
    align-items: start;
    padding: 1.5rem;
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: 18px;
    background: linear-gradient(135deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.03));
    box-shadow: 0 18px 50px rgba(0, 0, 0, 0.18);
  }

  .education-project-media {
    display: grid;
    gap: 1rem;
  }

  .education-project-image {
    display: block;
    width: 100%;
    border-radius: 12px;
    overflow: hidden;
    background: rgba(255, 255, 255, 0.04);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .education-project-image:hover {
    transform: translateY(-2px);
    box-shadow: 0 14px 32px rgba(0, 0, 0, 0.24);
  }

  .education-project-image img {
    display: block;
    width: 100%;
    height: auto;
  }

  .education-project-preview img {
    aspect-ratio: 16 / 9;
    object-fit: cover;
  }

  .education-project-card h2 {
    margin-top: 0;
    margin-bottom: 0.75rem;
  }

  .education-project-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin-top: 1rem;
  }

  .education-project-actions a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-width: 8.5rem;
    padding: 0.65rem 1rem;
    border-radius: 999px;
    text-decoration: none;
    font-weight: 600;
  }

  .education-project-actions a:first-child {
    background: #ffb347;
    color: #1f1f1f;
  }

  @media (max-width: 800px) {
    .education-project-card {
      grid-template-columns: 1fr;
    }
  }
</style>

This is an overview of my educational open source projects

<div class="education-project-list">
  {% for project in site.data.education_projects %}
    <article class="education-project-card">
      <div class="education-project-media">
        <a class="education-project-image" href="{{ project.github_url }}" target="_blank" rel="noopener noreferrer">
          <img src="{{ project.repo_card_url }}" alt="{{ project.name }} GitHub repository card">
        </a>
        <a class="education-project-image education-project-preview" href="{{ project.project_url }}" target="_blank" rel="noopener noreferrer">
          <img src="{{ project.preview_image_url }}" alt="{{ project.name }} live project preview">
        </a>
      </div>
      <div>
        <h2>{{ project.name }}</h2>
        <p>{{ project.description }}</p>
        <div class="education-project-actions">
          <a href="{{ project.project_url }}" target="_blank" rel="noopener noreferrer">Try it out</a>
        </div>
      </div>
    </article>
  {% endfor %}
</div>

All of my education projects on [GitHub](https://github.com/Peaj?tab=repositories&q=education&type=public&language=&sort=)