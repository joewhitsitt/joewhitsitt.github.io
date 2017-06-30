---
title: Tubing
weight: 4
permalink: /tubing/
---
<p>For those of you haven't been tubing before, or need a friendly reminder:</p>
<div id="accordion" role="tablist" aria-multiselectable="true">
{% for item in site.data.tubing %}
  <div class="card">
    <div class="card-header" role="tab" id="heading{{ item.key }}">
      <h5 class="mb-0">
        <a data-toggle="collapse" data-parent="#accordion" href="#collapse{{ item.key }}" aria-expanded="false" aria-controls="collapse{{ item.key }}">
          {{ item.title }}
        </a>
      </h5>
    </div>

    <div id="collapse{{ item.key }}" class="collapse" role="tabpanel" aria-labelledby="heading{{ item.key }}">
      <div class="card-block">
        {{ item.content }}
      </div>
    </div>
  </div>
{% endfor %}
</div>
