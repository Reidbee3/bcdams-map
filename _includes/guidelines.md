{% assign element = site.data.elements[page.data] %}

# {{ element.label }}

__URI:__ <{{ site.url }}#{{ element.name }}>

__Definition:__ {{ element.definition }}

{% if element.same_as_uri %}__Same As:__ <{{ element.same_as_uri }}>

{% endif %}__Obligation:__ {% include obligation_label.md %}

__Repeatable:__ {% if element.repeatable == true %}True{% else %}False{% endif %}

__Range:__ {% for r in element.range %}{% if r.uri %}[{{ r.label }}]({{ r.uri }})  {% else %}{{ r.label }}{% endif %}{% endfor %}

---

## Input Guidelines
