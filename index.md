---
layout: default
---

<!-- <header>
    <a href="/join" class="join-button" target="_blank">Join us</a>
</header> -->

<div class="intro-header">
    <!-- <div class="container"> -->
        <h1 class="heading-jumbo">Ambitious</h1>
        <h4 class="subheading">Community and resources for young people in science and tech.</h4>
    <!-- </div> -->
</div>

<!-- <div class="pull-up"> -->
<!-- Header -->
<div class="container">
    <div class="motto-wrap">
        <!--<div class="relaunch">
            <h3><span>🚀 Ambitious 2.0 is here. <a href="#">Find out what's new &rarr;</a></span></h3>
        </div>-->
        <h2>We're a community of engineers, researchers, and builders interested in science and tech.</h2>
        <p>Ambitious is creating a space for exceptional young people to collaborate on projects, have conversations, make friends, and <span>build a competitive advantage</span>. We believe investing in these people early will have compounding returns over the long run, pushing science and technology forward.</p>
    </div>
</div>

<!-- Offer -->
<div class="container">
    <div class="divider"></div>
    <div class="offer">
        <div class="col">
            <div class="label">NETWORK</div>
            <h2>Community</h2>
            <p class="light">We host a Discord server for community members to hang out and chat about whatever they're interested in. Topics range from AI to healthcare, music, and beyond.</p>
        </div>
        <div class="col">
            <div class="label">SPEAKERS</div>
            <h2>Weekly Brew</h2>
            <p class="light">On Sundays, we invite an interesting guest for a private interview and AMA session. Community members compile questions throughout the week, and can ask their own questions directly during Q&A.</p>
        </div>
        <div class="col">
            <div class="label">ADVANTAGE</div>
            <h2>Resources</h2>
            <p class="light">We source opportunities and resources to help members get a leg up in their careers and on their projects. This could be a key mentor or cloud hosting credits - whatever you need.</p>
        </div>
    </div>
    <div class="divider"></div>
</div>

<!-- Weekly Brew -->
{% assign speakers = site.speakers | sort: 'date' | reverse %}
<div class="container">
    <div class="weekly-brew">
        <!-- <div class="up-next">
            <div class="col-4">
                {% if speakers.first.image contains '://' %}
                    <img src="{{ speakers.first.image }}" />
                {% else %}
                    <img src="{{ speakers.first.image | prepend: site.url }}" />
                {% endif %}
            </div>
            <div class="col-8">
                <div class="label">UP NEXT</div>
                <h2 class="speaker-name">{{ speakers.first.name }}</h2>
                <div class="light">{{ speakers.first }}</div>
            </div>
        </div> -->
        <div class="past-speakers-wrapper">
            <!-- <div class="label">PAST SPEAKERS</div> -->
            <h2>Past speakers</h2>
            <div class="speakers">
                {% for speaker in speakers %}
                    {% if speaker != speakers.first %}
                        <div class="item">
                            {% if speaker.image contains '://' %}
                                <img src="{{ speaker.image }}" />
                            {% else %}
                                <img src="{{ speaker.image | prepend: site.url }}" />
                            {% endif %}
                            <div class="speaker-name">{{ speaker.name }}</div>
                        </div>
                    {% endif %}
                {% endfor %}
            </div>
        </div>
    </div>
    <div class="divider"></div>
</div>
<!-- </div> -->

<!-- Contact -->
<div class="container">
    <div class="contact">
        <h2>Interested? <a href="https://twitter.com/messages/compose?recipient_id=708807667335241729&text=Interested+in+ambitious.guide!">Apply to join us &rarr;</a></h2>
        <h3>Get in touch at <a href="mailto:hello@ambitious.guide">hello@ambitious.guide</a>, or via <a href="https://twitter.com/c3kel" target="_blank">Twitter</a>.</h3>
    </div>
</div>
