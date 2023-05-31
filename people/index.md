---
layout: default
---

# People: Core contributors

The Public & Open Foundation draws on a multidisciplinary network of contributors. It is spearheaded by members of the leadership team from the Foundation for Public Code.

## Core contributors

<style>
    main .content {
        width: 100%;
        flex: 1 1 100%;
    }
    #core-contributors-list {
        list-style: none;
        padding: 0 0 0 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        align-items: first baseline;
        max-width: 100%;
        background-color: whitesmoke;
    }
    #core-contributors-list>li {
        display: block;
        max-width: 165px;
        width: 100%;
        max-width: 20em;
        margin: 1em;
    }
    #core-contributors-list>li>a>svg {
        display: block;
        width: 100%;
        background-color: #5B57CA
    }
    #core-contributors-list>li>a>h3,
    #core-contributors-list>li>a>p {
        text-decoration: none;
    }
    .markdown-body li + li {
        margin-top: 0;
    }
</style>

<ul id="core-contributors-list">
{% assign bios = site.pages | where: 'type', 'Bio' %}
{% for bio in bios %}
<li>
    <a href="{{bio.url}}">
        <svg viewBox="0 0 100 100">
    {% if bio.image %}
            <image href="core-contributors/{{bio.image}}" alt="Photo of {{bio.title}}" height="100" width="100" preserveAspectRatio="xMidYMid slice"/>
    {% endif %}
        </svg>
    </a>
    <h3><a href="{{bio.url}}">{{ bio.title }}</a></h3>
    <p>{{ bio.role }}</p>
</li>
{% endfor %}
</ul>
