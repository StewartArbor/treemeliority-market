---
title: Treemeliority Market
description: Useful necessities and improbable objects for people interested in trees, animals, fieldwork, and the physical world.
lang: en
---

<section class="market-hero">
  <div class="shell">
    <p class="eyebrow">TREEMELIORITY MARKET</p>
    <h1>Things that earn<br>their existence.</h1>
    <p class="lead">Two shelves. One contains things you will probably need anyway. The other contains things that had no obligation to exist, but improve the world by having done so.</p>
  </div>
</section>

<section class="market-switcher shell" aria-label="Market sections">
  <input class="market-radio" type="radio" name="market-tab" id="tab-essentials" checked>
  <input class="market-radio" type="radio" name="market-tab" id="tab-curiosities">

  <div class="market-tabs" role="tablist" aria-label="Browse Treemeliority Market">
    <label for="tab-essentials" id="essentials" role="tab">
      <span>01</span>
      <strong>ESSENTIALS</strong>
      <small>Things that solve recurring problems.</small>
    </label>
    <label for="tab-curiosities" id="curiosities" role="tab">
      <span>02</span>
      <strong>CURIOSITIES</strong>
      <small>Things that did not need to exist, but fortunately do.</small>
    </label>
  </div>

  <div class="market-panels">
    <section class="market-panel essentials-panel" aria-labelledby="essentials">
      <div class="panel-intro">
        <p class="eyebrow">LOW-SYMBOLISM · HIGH-USE</p>
        <h2>Small infrastructure for ordinary life.</h2>
        <p>Objects that are repeatedly used, lost, worn out, replaced, or required for maintenance. Cheapness is useful here only when failure is boring rather than catastrophic.</p>
      </div>

      {% assign essential_products = site.data.products | where: "active", true | where: "shelf", "essentials" %}
      {% if essential_products.size > 0 %}
      <div class="product-grid">
        {% for product in essential_products %}
        {% include product-card.html product=product %}
        {% endfor %}
      </div>
      {% else %}
      <div class="empty-shelf">
        <strong>The shelf is being stocked.</strong>
        <p>No placeholder merchandise. Products appear here only after a real merchant link has been checked and added to the catalogue.</p>
      </div>
      {% endif %}
    </section>

    <section class="market-panel curiosities-panel" aria-labelledby="curiosities">
      <div class="panel-intro">
        <p class="eyebrow">DELIGHTFUL NON-NECESSITIES</p>
        <h2>Objects with an alibi, not a defence.</h2>
        <p>Selected for conceptual strangeness, visual ingenuity, optical trickery, or because some engineer looked at an ordinary problem and chose a wonderfully disproportionate solution.</p>
      </div>

      {% assign curiosity_products = site.data.products | where: "active", true | where: "shelf", "curiosities" %}
      {% if curiosity_products.size > 0 %}
      <div class="product-grid curiosity-products">
        {% for product in curiosity_products %}
        {% include product-card.html product=product %}
        {% endfor %}
      </div>
      {% else %}
      <div class="empty-shelf dark">
        <strong>The cabinet is presently empty.</strong>
        <p>Curiosities will appear here as soon as they have a real merchant destination. No spectral products will be summoned merely to decorate the page.</p>
      </div>
      {% endif %}
    </section>
  </div>
</section>

<section class="field-notes section">
  <div class="shell">
    <div class="section-head">
      <div><p class="eyebrow">FIELD NOTES</p></div>
      <div>
        <h2>Before the affiliate link comes the mechanism.</h2>
        <p>Short guides on what specifications actually change, where cheap equipment is rational, and where bargain hunting merely purchases a more interesting failure mode.</p>
      </div>
    </div>

    <div class="guide-grid">
      <a class="guide-link" href="/guides/binoculars/"><span>01</span><b>Choosing binoculars for birds and wildlife</b></a>
      <a class="guide-link" href="/guides/hand-lens/"><span>02</span><b>Field hand lenses: magnification and working distance</b></a>
      <a class="guide-link" href="/guides/plant-care-tools/"><span>03</span><b>A minimal tool kit for propagation and plant care</b></a>
      <a class="guide-link" href="/guides/weather-stations/"><span>04</span><b>Home weather stations: which sensors are worth having</b></a>
      <a class="guide-link" href="/guides/field-notebook/"><span>05</span><b>The field notebook as a system of record</b></a>
      <a class="guide-link" href="/editorial-policy/"><span>06</span><b>How we choose: function, failure modes, and affiliate separation</b></a>
    </div>
  </div>
</section>