---
title: Welcome to my Website!
description: FoxSylv's Website
keywords: [foxsylv]
css: index.css
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
            <img class="social-icon to-beige" src="{{ "assets/youtube-icon.svg" | relative_url }}">
        </a>
        <a title="Speedrun.com" href="https://www.speedrun.com/user/FoxSylv" target="_blank" rel="noopener noreferrer">
             <img class="social-icon to-beige" src="{{ "assets/speedrun-icon.svg" | relative_url }}">
        </a>
        <a title="Github" href="https://github.com/FoxSylv1" target="_blank" rel="noopener noreferrer">
            <img class="social-icon to-beige" src="{{ "assets/github-icon.svg" | relative_url }}">
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
    <div class="project box">
    </div>
    <div class="project box">
        <p>
            There's nothing here yet!
            <br>
            Try coming back later! ^w^
        </p>
    </div>
    <div class="project box">
    </div>
</div>

<div class="centered-text space50px">
    <h2>
        Videos
    </h2>
</div>
<div class="flex full-width space210px">
    <div class="box">
        <div class="space20px"></div>
        <p class="space40px">
            Good Videos!
        </p>
        <iframe class="video-player" src="https://www.youtube-nocookie.com/embed/videoseries?list=PLP7958ucW5B94tgKYTYJOhyiKdbz1-BrF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="box">
        <div class="space20px"></div>
        <p class="space40px">
            Speedruns/Accomplishments!
        </p>
        <iframe class="video-player" src="https://www.youtube-nocookie.com/embed/videoseries?list=PLP7958ucW5B9t-99OgP47cd9ymRq8Ut2M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
</div>
