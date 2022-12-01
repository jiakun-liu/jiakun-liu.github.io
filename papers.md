---
layout: page
title: Publications
permalink: /publications/
---

<section class="section projects-section">
    {% for year in site.data.papers %}
        <div class="intro">
            <p class="section-title">{{year[0]}}</p>
        </div><!--//intro-->
        {% for paper in year[1] %}
                <div class="item">
                <span class="project-tagline">[{{paper.idx}}] {{ paper.authors }}. "{{ paper.title }}" <em>{{ paper.venue }}</em>, {{paper.status}}</span>
                {% if paper.remark%}
                    (<span class="project-tagline"><b>{{ paper.remark }}</b></span>)
                {% endif %}
                {% if paper.pdf%}
                    <span class="pull-right"> <a href="{{ site.url }}/{{ paper.pdf }}"><b>[PDF]</b></a></span>
                {% endif %}
                </div>
        {% endfor %}
    {% endfor %}
   
</section><!--//section-->