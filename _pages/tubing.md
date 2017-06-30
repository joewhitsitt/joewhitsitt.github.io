---
title: Tubing
weight: 4
permalink: /tubing/
---
<p>For those of you haven't been tubing before, or need a friendly reminder</p>
{% assign tubing = site.data.tubing | sort: 'id' %}
<div id="accordion" role="tablist" aria-multiselectable="true">
{% for item in tubing %}
  <div class="card">
    <div class="card-header" role="tab" id="heading{{ item.id }}">
      <h5 class="mb-0">
        <a data-toggle="collapse" data-parent="#accordion" href="#collapse{{ item.id }}" aria-expanded="false" aria-controls="collapse{{ item.id }}">
          {{ item.title }}
        </a>
      </h5>
    </div>

    <div id="collapse{{ item.id }}" class="collapse" role="tabpanel" aria-labelledby="heading{{ item.id }}">
      <div class="card-block">
        {{ item.content }}
      </div>
    </div>
  </div>
{% endfor %}
</div>
