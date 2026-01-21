---
layout: default 
title: Schedule
nav_order: 3
---

# Semester Schedule

The schedule will be flexible as we cover each topic. We might spend some extra time on topics, so we will update the schedule as we progress through the semester.

<table class="schedtab"><thead>
<tr>
    <th>Mtg</th>
    <th>Date</th>
    <th>Topic</th>
    <th>Notes</th>
    </tr>
    </thead>
    <tbody><!--  {% increment lab %} {% increment mtg %} -->
{% for day in site.data.schedule %}
{% if day.type == 'holiday' or day.type == 'labholiday' %}
<tr class="holiday">
{% elsif day.type == 'header' %}
<tr class="header">
{% elsif day.type == 'lab' %}
<tr class="lab">
{% elsif day.type == 'exam' %}
<tr class="exam">
{% else %}
<tr>
{% endif %}
    {% if day.type == 'lab' %}
            <td class="lab mtg">LAB {% increment lab %}
            {% elsif day.type == 'header'%}
            <td class="header mtg">
            {% elsif day.type == 'holiday'%}
            <td class="holiday mtg">
            {% elsif day.type == 'labholiday'%}
            <td class="holiday mtg">LAB
            {% elsif day.type == 'exam'%}
            <td class="exam mtg">
            {% else %}
            <td class="mtg">
                {% increment mtg %}
            {% endif %}</td>
    <td class="text-center sched">{{day.date}}</td>
    <td class="sched">
    {% if day.link %}
        <a href="{{day.link}}">
    {% endif %}
    {{day.topic}}
    {% if day.link %}
        </a>
    {% endif %}
    {% if day.lectures or day.readings or day.activities %}
    <br><span class="sched-sub">
        {% if day.readings %}
        Readings:
        {% for read in day.readings %}
        {% unless forloop.first %}
        -
        {% endunless %}
        {% if read.link %}
        <a href="{{read.link}}">
        {% endif %} 
        {{read.topic}}
        {% if read.link %}
        </a> 
        {% endif %}
        {% endfor %}
        {% endif %}
        {% if day.lectures and day.readings %}
        <br>
        {% endif %}
        {% if day.lectures %}
        Slides:
        {% for pdf in day.lectures %}
        {% unless forloop.first %}
        -
        {% endunless %}
        {% if pdf.link %}
        <a href="{{pdf.link}}" alt="{{pdf.alt}}">{{pdf.time}}</a> 
        {% else %}
        <span title="{{pdf.alt}}">{{pdf.time}}</span> 
        {% endif %}
        {% endfor %}
        {% endif %}

        {% if day.videos %}
        <br>
        Videos:
        {% for vid in day.videos %}
        {% unless forloop.first %} - {% endunless %}
        <a href="{{vid.link}}">{{vid.name}}</a>
        {% endfor %}
        {% endif %}


        {% if (day.lectures or day.readings) and day.activities %}
        <br>
        {% endif %}
        {% if day.activities %}
        {% assign date_parts = day.date | split: "/" %}
        {% assign schedule_month = date_parts[0] | plus: 0 %}
        {% assign schedule_day = date_parts[1] | plus: 0 %}
        {% assign schedule_year = date_parts[2] | plus: 0 %}
        {% assign schedule_timestamp = schedule_year | times: 10000 | plus: schedule_month | times: 100 | plus: schedule_day %}
        {% assign today_year = site.time | date: "%Y" | plus: 0 %}
        {% assign today_month = site.time | date: "%m" | plus: 0 %}
        {% assign today_day = site.time | date: "%d" | plus: 0 %}
        {% assign today_timestamp = today_year | times: 10000 | plus: today_month | times: 100 | plus: today_day %}
        {% if schedule_timestamp <= today_timestamp %}
        In-Class Activity:
        {% for pdf in day.activities %}
        {% unless forloop.first %}
        -
        {% endunless %}
        {% if pdf.link %}
        <a href="{{pdf.link}}" alt="{{pdf.alt}}">{{pdf.name}}</a> 
        {% else %}
        <span title="{{pdf.alt}}">{{pdf.name}}</span> 
        {% endif %}
        {% endfor %}
        {% endif %}
        {% endif %}
        </span>
    {% endif %}
    </td>
    <td class="sched">{{day.notes}}</td>
    </tr>
{% endfor %}
</tbody></table>