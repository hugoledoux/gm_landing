---
layout: default
---

<div class="row">

  {% for cat in site.data.links %}
  <div class="col-4"> 
    <div class="card">
      <header><h4>{{ cat.category }}</h4></header>
      {% for each in cat.links %}
        <a href="{{each.url}}">{{each.name}}</a>
        {% if each.extra %}
          &emsp;{{each.extra}}
        {% endif %}
        <br>
      {% endfor %}
    </div>
  </div>
  {% endfor %}

</div>

