---
layout: page
---

<header class="intro">
  <div class="intro-body">
    <div class="container">
      <div class="row">
        <div class="col-md-8 col-md-offset-2">
          {% assign intro = site.kultavilla | where:"name", "intro"  | first %}
          {{ intro }}
        </div>
      </div>
    </div>
  </div>
</header>

<section id="slogan" class="content-section text-center">
  <div class="slogan-section">
    <div class="container">
      <div class="col-lg-8 col-lg-offset-2">
        {% assign tpl = site.kultavilla | where:"name", "slogan"  | first %}
        {{ tpl }}
      </div>
    </div>
  </div>
</section>

<section id="services" class="container content-section">
  <div class="services-section">
    <div class="container">
      <div class="col-md-4">
        {% assign tpl = site.kultavilla | where:"name", "services-design"  | first %}
        {{ tpl }}
      </div>
      
      <div class="col-md-4">
        {% assign tpl = site.kultavilla | where:"name", "services-production"  | first %}
        {{ tpl }}
      </div>
      
      <div class="col-md-4">
        {% assign tpl = site.kultavilla | where:"name", "services-product-development"  | first %}
        {{ tpl }}
      </div>
    </div>
  </div>
</section>

<section id="references" class="container content-section">
  <div class="references-section">
    <div class="container">
      {% assign references = site.kultavilla | where:"name", "references"  | first %}
      {{ references }}

      {% for ref in references.references %}
      <div class="col-lg-4 col-sm-6 portfolio-box">
        <img src="{{ site.baseurl }}/{{ ref.img_image }}" class="img-responsive" alt="">
        <div class="portfolio-box-caption">
          <div class="portfolio-box-caption-content">
            <h5>{{ ref.title }}</h5>
            {{ ref.description_text | markdownify }}
          </div>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<section id="contact" class="container content-section">
  <div class="contact-section">
    <div class="container">

      <div class="col-lg-8">
        {% assign tpl = site.kultavilla | where:"name", "contact"  | first %}
        {{ tpl }}
        <ul class="list-inline social-buttons">
          <li><a href="#" title="Instagram"><i class="fa fa-instagram"></i></a></li>
          <li><a href="#" title="YouTube"><i class="fa fa-youtube"></i></a></li>
        </ul>
      </div>

      <div class="col-lg-12">
        <div class="text-center">
          {% assign workshop = site.kultavilla | where:"name", "workshop"  | first %}
          {{ workshop }}
        </div>

        {% for image in workshop.images %}
        <div class="col-lg-4 col-md-6 col-xs-12 thumb">
          <span class="thumbnail">
            <img class="img-responsive" src="{{ site.baseurl }}/{{ image.img_image }}" alt="">
          </span>
        </div>
        {% endfor %}

        <div class="col-lg-4 col-md-6 col-xs-12 thumb">
          <span class="thumbnail">
            <iframe src="https://player.vimeo.com/video/119056274" width="100%" height="400" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
          </span>          
        </div>
      </div>
    </div>
  </div>
</section>
