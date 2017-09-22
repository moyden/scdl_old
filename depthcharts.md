---
layout: depth
permalink: /depth-chart
---

<section>
    <table>
    <tr>
        <th class="title">Depth Charts</th>
        <th class="fifth">QB</th><th class="dollar">$</th><th class="yr">yr</th>
        <th class="fifth">RB</th><th class="dollar">$</th><th class="yr">yr</th>
        <th class="fifth">WR</th><th class="dollar">$</th><th class="yr">yr</th>
        <th class="fifth">TE</th><th class="dollar">$</th><th class="yr">yr</th>
    </tr>
    {% for team in site.data.rosters %}
    <tr id="{{ team.id }}-exp">
        <td>
            <p>{{ team.name }}</p>
            <p class="team-owner">{{ team.owner }}</p>
        </td>
        <td class="name">
          {% for player in team.roster %}
            {% if player.posi == "QB" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.name }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="cost">
            {% for player in team.roster %}
            {% if player.posi == "QB" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.cost }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="year">
            {% for player in team.roster %}
            {% if player.posi == "QB" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {% if player.cost %}
                      {{ player.year }}
                      {% else %}
                      &nbsp;
                      {% endif %}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="name">
          {% for player in team.roster %}
            {% if player.posi == "RB" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.name }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="cost">
            {% for player in team.roster %}
            {% if player.posi == "RB" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.cost }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="year">
            {% for player in team.roster %}
            {% if player.posi == "RB" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {% if player.cost %}
                      {{ player.year }}
                      {% else %}
                      &nbsp;
                      {% endif %}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="name">
          {% for player in team.roster %}
            {% if player.posi == "WR" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.name }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="cost">
            {% for player in team.roster %}
            {% if player.posi == "WR" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.cost }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="year">
            {% for player in team.roster %}
            {% if player.posi == "WR" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {% if player.cost %}
                      {{ player.year }}
                      {% else %}
                      &nbsp;
                      {% endif %}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="name">
          {% for player in team.roster %}
            {% if player.posi == "TE" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.name }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="cost">
            {% for player in team.roster %}
            {% if player.posi == "TE" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {{ player.cost }}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
        <td class="year">
            {% for player in team.roster %}
            {% if player.posi == "TE" %}
              <ul>
                {% unless player.drop %}
                  <li>
                      {% if player.cost %}
                      {{ player.year }}
                      {% else %}
                      &nbsp;
                      {% endif %}
                  </li>
                {% endunless %}
              </ul>
            {% endif %}
          {% endfor %}
        </td>
    </tr>
    {% endfor %}
    </table>
</section>