---
layout: docs
title: Badges
description: Documentation and examples for badges, our small count and labeling component.
group: components
toc: true
---

## Example

{% capture example %}
<div class="white-bg p-9">
    <div class="icons-group py-1 px-2">
        <span class="icn-globe mr-2"></span>
        <span class="icn-email mr-2"></span>
        <span class="icn-clipboard"></span>
    </div>
</div>
{% endcapture %}
{% include example.html content=example %}

Badges can be used as part of links or buttons to provide a counter.

{% capture example %}
<button type="button" class="btn btn-primary">
  Notifications <span class="badge badge-light">4</span>
</button>
{% endcapture %}
{% include example.html content=example %}

Note that depending on how they are used, badges may be confusing for users of screen readers and similar assistive technologies. While the styling of badges provides a visual cue as to their purpose, these users will simply be presented with the content of the badge. Depending on the specific situation, these badges may seem like random additional words or numbers at the end of a sentence, link, or button.

Unless the context is clear (as with the "Notifications" example, where it is understood that the "4" is the number of notifications), consider including additional context with a visually hidden piece of additional text.

{% capture example %}
<button type="button" class="btn btn-primary">
  Profile <span class="badge badge-light">9</span>
  <span class="sr-only">unread messages</span>
</button>
{% endcapture %}
{% include example.html content=example %}

## Contextual variations

Add any of the below mentioned modifier classes to change the appearance of a badge.

{% capture example %}
{% for color in site.data.theme-colors %}
<span class="badge badge-{{ color.name }}">{{ color.name | capitalize }}</span>{% endfor %}
{% endcapture %}
{% include example.html content=example %}

{% include callout-warning-color-assistive-technologies.md %}

## Pill badges

Use the `.badge-pill` modifier class to make badges more rounded (with a larger `border-radius` and additional horizontal `padding`). Useful if you miss the badges from v3.

{% capture example %}
{% for color in site.data.theme-colors %}
<span class="badge badge-pill badge-{{ color.name }}">{{ color.name | capitalize }}</span>{% endfor %}
{% endcapture %}
{% include example.html content=example %}

## Links

Using the contextual `.badge-*` classes on an `<a>` element quickly provide _actionable_ badges with hover and focus states.

{% capture example %}
{% for color in site.data.theme-colors %}
<a href="#" class="badge badge-{{ color.name }}">{{ color.name | capitalize }}</a>{% endfor %}
{% endcapture %}
{% include example.html content=example %}
