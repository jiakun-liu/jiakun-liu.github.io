---
layout: page
title: Services
permalink: /service/
---

<section class="section projects-section">

   {% for year in site.data.services %}
        <div class="intro">
            <p class="section-title">{{year[0]}}</p>
        </div><!--//intro-->
        {% for service in year[1] %}
         <div class="item">  
            {{service.name}} -- {{service.venue}}
         </div> 
        {% endfor %}
    {% endfor %}


   
</section><!--//section-->
