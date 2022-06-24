---
title: Welcome to my Website!
description: FoxSylv's Website
keywords: [foxsylv]
css: [index.css, project-display.css]
---

<div class="flex full-width space200px">
    <div id="title">
        <h1>
            FoxSylv
        </h1>
        <br>
        <p id="subtitle">
            nya nya foxgirl uwu
        </p>
    </div>
    
    <div id="social-icons">
        <a title="Youtube" href="https://www.youtube.com/channel/UCj7lR9rm06lCxE4kxkJeECA" target="_blank" rel="noopener noreferrer">
            <img class="social-icon to-beige" src="{{ "assets/site-icons/youtube-icon.svg" | relative_url }}">
        </a>
        <a title="Speedrun.com" href="https://www.speedrun.com/user/FoxSylv" target="_blank" rel="noopener noreferrer">
             <img class="social-icon to-beige" src="{{ "assets/site-icons/speedrun-icon.svg" | relative_url }}">
        </a>
        <a title="Github" href="https://github.com/FoxSylv1" target="_blank" rel="noopener noreferrer">
            <img class="social-icon to-beige" src="{{ "assets/site-icons/github-icon.svg" | relative_url }}">
        </a>
    </div>
</div>


<div class="centered-text space160px">
    <h3>
        Hello!
        <br>
    </h3>
    <p>
        Welcome to my website!
    </p>
</div>
<div class="centered-text space200px">
    <p>
        This is the corner of the internet where I put my things.
        <br>
        They're not the greatest things, but they're special because I made them.
        <br>
        Feel free to take a look around at my things, if you would like!
    </p>
</div>

<div class="flex full-width" id="down-arrow-container">
    <div>
        <img id="down-arrow" class="to-beige" src="{{ "assets/down-arrow.svg" | relative_url }}">
        <script>
            function setOpacity(opacity) {
                var downArrow = document.getElementById("down-arrow");
                downArrow.style.opacity = opacity;
            }
            function changeOpacityOnScroll() {
                setOpacity((70 - this.scrollY) / 70);
            }
            
            setOpacity(1);
            window.addEventListener("scroll", changeOpacityOnScroll, false);
        </script>
        <!-- Default noscript behaviour is no arrow being visible -->
    </div>
</div>

<div class="centered-text space50px">
    <div>
        <h2>
            Projects
        </h2>
    </div>
</div>
<div class="flex full-width space150px">
    {% for project_data in site.data.project_data_list %}
        {% if project_data.isImportant == 'true' %}
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
        {% endif %}
    {% endfor %}
    <div class="flex project box" id="project-more">
        <a href="{{ "/projects/" | relative_url }}">
            <h2>
                More!
            </h2>
        </a>
    </div>
</div>

<div class="centered-text space50px">
    <h2>
        Videos
    </h2>
</div>
<div class="flex full-width space210px">
    {% for youtube_data in site.data.youtube_data_list %}
        <div class="video-container box centered-text">
            <div class="space20px"></div>
            <h3>
                {{ youtube_data.title }}
            </h3>
            <div class="space30px"></div>
            <iframe class="video-player" src="{{ youtube_data.link }}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    {% endfor %}
</div>
