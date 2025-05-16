---
layout: archive
title: "Exploration"
permalink: /blog/
author_profile: true
---
<style>
  body, h1, h2, h3, h4, h5, h6, p, div, a, span {
    font-family: Arial, "Times New Roman", serif !important;
  }
</style>


<!-- 🔬 소개 제목 -->
## 🧠 My Informatics Skills
I apply a wide range of bioinformatics tools and pipelines for virus discovery, genome assembly, and data visualization.

<!-- 💡 카드 레이아웃 -->
<div style="display: flex; flex-wrap: wrap; gap: 1.5rem; margin-bottom: 3rem;">

  <!-- Card 1 -->
  <div style="flex: 1 1 250px; border: 1px solid #ddd; border-radius: 10px; padding: 1.2rem; box-shadow: 2px 2px 8px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0;">🧬 Genomic Data Analysis</h3>
    <p style="margin-bottom: 0;">Experienced in processing RNA-seq, small RNA-seq, and viral metagenomic data using tools like <strong>STAR</strong>, <strong>Salmon</strong>, and <strong>SPAdes</strong>.</p>
  </div>

  <!-- Card 2 -->
  <div style="flex: 1 1 250px; border: 1px solid #ddd; border-radius: 10px; padding: 1.2rem; box-shadow: 2px 2px 8px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0;">🧪 Bioinformatics Pipelines</h3>
    <p style="margin-bottom: 0;">Built reproducible workflows using <strong>Snakemake</strong> and <strong>conda environments</strong> for virome profiling and genome annotation.</p>
  </div>

  <!-- Card 3 -->
  <div style="flex: 1 1 250px; border: 1px solid #ddd; border-radius: 10px; padding: 1.2rem; box-shadow: 2px 2px 8px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0;">📊 Data Visualization</h3>
    <p style="margin-bottom: 0;">Visualization with <strong>ggplot2</strong>, <strong>GraphPad</strong>, and <strong>R Shiny</strong> to interpret and present complex data sets effectively.</p>
  </div>

  <!-- Card 4 -->
  <div style="flex: 1 1 250px; border: 1px solid #ddd; border-radius: 10px; padding: 1.2rem; box-shadow: 2px 2px 8px rgba(0,0,0,0.05);">
    <h3 style="margin-top: 0;">🔍 Virus Discovery</h3>
    <p style="margin-bottom: 0;">Specialized in viral sequence mining from host transcriptomes, using <strong>DIAMOND BLASTx</strong> and custom <strong>viral domain annotation</strong>.</p>
  </div>

</div>

<!-- 📰 Exploration 카테고리의 포스트 목록 -->
{% for post in site.posts %}
  {% if post.categories contains "exploration" %}
  <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
    <div style="display: flex; align-items: center; margin-bottom: 2rem;">
      {% if post.image %}
        <div style="flex: 0 0 100px; margin-right: 1rem;">
          <img src="{{ post.image }}" alt="{{ post.title }}" style="width: 100px; border-radius: 4px;">
        </div>
      {% endif %}
      <div>
        <h2 class="archive__item-title no_toc" itemprop="headline">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <p class="page__meta">
          📅 {{ post.date | date: "%Y-%m-%d" }} • 🕒 {{ post.read_time | default: "1 minute" }} read
        </p>
        <p class="archive__item-excerpt" itemprop="description">
          {{ post.excerpt | strip_html | truncatewords: 25 }}
        </p>
      </div>
    </div>
  </article>
  {% endif %}
{% endfor %}
