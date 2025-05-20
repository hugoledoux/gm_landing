---
layout: default
---

<div class="row">

  {% for cat in site.data.links %}
  <div class="col-4"> 
    <div class="card">
      <header><h4>{{ cat.category }}</h4></header>
      <table class="striped ">
        <tbody>
        {% for each in cat.links %}
          <tr>
            <td><a href="{{each.url}}">{{each.name}}</a></td>
            <td >
            {% if each.extra %}
              &emsp;{{each.extra}}
            {% endif %}
            </td>
          <!-- <br> -->
          </tr>
        {% endfor %}
        </tbody>
      </table>
    </div>
  </div>
  {% endfor %}

</div>

