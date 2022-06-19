---
title: Projects I've Worked On!
description: A directory of projects that I've worked on.
keywords: [foxsylv, projects]
css: projects.css
permalink: /projects/
---

<div class="full-width centered-text space100px">
    <h1>
        Projects I've Worked On
    </h1>
</div>

<div class="flex" id="project-list">
    {% for project_data in site.data.project_data_list %}
        <div class="project box">
            <a href="{{ project_data.link | relative_url }}">
                <div class="project-title centered-text">
                    <h3>
                        {{ project_data.name }}
                    </h3>
                </div>
                <img class="project-image" src="{{ project_data.image | relative_url }}" alt="{{ project_data.name }} Image">
                <div class="project-description centered-text">
                    <p>
                        {{ project_data.description }}
                    </p>
                </div>
            </a>
        </div>
    {% endfor %}
</div>
