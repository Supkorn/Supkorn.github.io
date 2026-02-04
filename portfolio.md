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
    flex: 0 0 50%;
    max-width: 50%;
  }
  /* ตกแต่งหัวข้อหมวดหมู่ให้เด่นชัด */
  .category-header {
    padding: 80px 0 40px;
    background-color: #343a40; /* สีเข้มเพื่อให้ตัดกับพื้นหลัง */
    color: white;
    width: 100%;
    margin-top: 0;
  }
  .category-header h2 {
    font-size: 2.5rem;
    font-weight: 700;
  }
  @media (max-width: 768px) {
    .portfolio-item-custom {
      flex: 0 0 100%;
      max-width: 100%;
    }
  }
</style>

<section class="content-section" id="portfolio">
  <div class="container-fluid p-0">
    
    <div class="content-section-heading text-center" style="padding-top: 50px; padding-bottom: 50px;">
      <h3 class="text-secondary mb-0">คลังผลงาน</h3>
      <h2 class="mb-5">ผลงานทั้งหมดของปุณรดา</h2>
    </div>

    {% assign all_posts = site.posts | sort: 'date' | reverse %}

    <div id="learning-section" class="category-header text-center">
      <h2>🎓 Learning</h2>
      <p class="mb-0 text-faded">ด้านวิชาการและการเรียนรู้</p>
    </div>
    <div class="row no-gutters portfolio-grid">
      {% for post in all_posts %}
        {% if post.category == "Learning" %}
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
        {% endif %}
      {% endfor %}
    </div>

    <div id="arts-section" class="category-header text-center">
      <h2>🎨 Arts</h2>
      <p class="mb-0 text-faded">งานศิลปะและความคิดสร้างสรรค์</p>
    </div>
    <div class="row no-gutters portfolio-grid">
      {% for post in all_posts %}
        {% if post.category == "Arts" %}
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
        {% endif %}
      {% endfor %}
    </div>

    <div id="music-section" class="category-header text-center">
      <h2>🎶 Music</h2>
      <p class="mb-0 text-faded">ดนตรีไทยและเครื่องดนตรีสากล</p>
    </div>
    <div class="row no-gutters portfolio-grid">
      {% for post in all_posts %}
        {% if post.category == "Music" %}
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
        {% endif %}
      {% endfor %}
    </div>

    <div id="activities-section" class="category-header text-center">
      <h2>🌟 Activities</h2>
      <p class="mb-0 text-faded">กิจกรรมและการเรียนรู้นอกห้องเรียน</p>
    </div>
    <div class="row no-gutters portfolio-grid">
      {% for post in all_posts %}
        {% if post.category == "Activities" %}
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
        {% endif %}
      {% endfor %}
    </div>

    <div class="text-center mt-5 mb-5">
      <a class="btn btn-dark btn-xl" href="{{ '/' | relative_url }}">
        <i class="fa fa-arrow-left mr-2"></i> กลับหน้าหลัก
      </a>
    </div>
  </div>
</section>