---
layout: page
---
<header class="intro">
  <div class="intro-body">
    <div class="container">
      <div class="row">
        <div class="col-md-8 col-md-offset-2">
          <p class="intro-text">{{ site.data.kultavilla.header }}</p>
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
      {% assign tpl = site.kultavilla | where:"name", "references"  | first %}
      {{ tpl }}

      {% assign refs = (site.references | sort: "position") %}
      
      {% for ref in refs %}
      <div class="col-lg-4 col-sm-6 portfolio-box">
        <img src="{{ site.baseurl }}/uploads/{{ ref.img_image }}" class="img-responsive" alt="">
        <div class="portfolio-box-caption">
          <div class="portfolio-box-caption-content">
            {{ ref.content }}
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
          {% assign tpl = site.kultavilla | where:"name", "workshop"  | first %}
          {{ tpl }}
        </div>
        {% for image in site.static_files %}
        {% if image.path contains 'images/workshop-' %}
        <div class="col-lg-4 col-md-6 col-xs-12 thumb">
          <span class="thumbnail">
            <img class="img-responsive" src="{{ site.baseurl }}/{{ image.path }}" alt="">
          </span>
        </div>
        {% endif %}
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
