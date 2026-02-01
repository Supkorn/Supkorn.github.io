---
layout: default
title: "All Projects"
permalink: /portfolio/
---

<style>
  .portfolio-grid {
    display: flex;
    flex-wrap: wrap;
    margin: 0;
    padding: 0;
  }
  .portfolio-item-custom {
    flex: 0 0 50%; /* บังคับให้กินพื้นที่ 50% หรือ 2 คอลัมน์ */
    max-width: 50%;
  }
  @media (max-width: 768px) {
    .portfolio-item-custom {
      flex: 0 0 100%; /* ในมือถือให้เป็นคอลัมน์เดียว */
      max-width: 100%;
    }
  }
</style>

<section class="content-section" id="portfolio">
  <div class="container-fluid p-0"> <div class="content-section-heading text-center">
      <h3 class="text-secondary mb-0">คลังผลงาน</h3>
      <h2 class="mb-5">ผลงานทั้งหมดของปุณรดา</h2>
    </div>
    
    <div class="row no-gutters portfolio-grid">
      {% assign mid = site.posts | sort: 'date' %}
      {% assign all_posts = mid | reverse %}
      
      {% for post in all_posts %}
        <div class="portfolio-item-custom"> 
          <a class="portfolio-item" href="{{ post.url | relative_url }}">
            <span class="caption">
              <span class="caption-content">
                <h2>{{ post.title | escape }}</h2>
                <p class="mb-0">{{ post.subtitle | escape }}</p>
              </span>
            </span>
            <img class="img-fluid" src="{{ site.baseurl }}/assets/img/{{ post.poster }}" alt="{{ post.title }}" style="width: 100%;">
          </a>
        </div>
      {% endfor %}
    </div>

    <div class="text-center mt-5 mb-5">
      <a class="btn btn-dark btn-xl" href="{{ '/' | relative_url }}">
        <i class="fa fa-arrow-left mr-2"></i> กลับหน้าหลัก
      </a>
    </div>
  </div>
</section>