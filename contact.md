---
title: Contact Me!
description: Contact me! Or don't! I don't mind either way :)
keywords: [foxsylv, contact]
css: contact.css
permalink: /contact/
---

<div class="full-width centered-text space100px">
    <h1>
        Contact Me!
    </h1>
</div>

<div class="space100px">
    {% for contact_data in site.data.contact_data_list %}
        <div class="contact-data box">
            <img class="contact-icon to-beige" src="{{ contact_data.image | relative_url }}" title="{{ contact_data.site }}" alt="{{ contact_data.site }} Icon">
            <h2>
                {{ contact_data.site }}
            </h2>
            <p>
                <a href="{{ contact_data.link }}" target="_blank" rel="noopener noreferrer">
                    {{ contact_data.username }}
                </a>
            </p>
            <br>
            <p>
                {{ contact_data.description }}
            </p>
        </div>
    {% endfor %}
</div>
