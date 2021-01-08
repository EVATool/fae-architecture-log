---
layout: default
---

<h1>Overview on all Decisions</h1>

This is the architectural decision log for the FAE course.

<table>
    <thead>
    <tr>
        <th width="8%">Status</th>
        <th width="60%">Title</th>
        <th width="15%">Responsible</th>
        <th width="15%">Deadline</th>
    </tr>
    </thead>
    <tbody>
        {% for decision in site.decisions %}
        <tr>
            {% include /functions/get-status-infos.html mydecision=decision %}
            <td><img class={{ status_class }} src="{{ site.url }}{{ status_filename | relative_url }}"/></td>
            <td>{{ decision.title }}</td>
            <td>{{ decision.responsible }}</td>
            <td>{{ decision.deadline }}</td>
        </tr>
        {% endfor %}
    </tbody>
</table>

