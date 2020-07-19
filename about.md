---
layout: page
i18n_title: pages.about
titles:
  pt      : &PT       Sobre
  pt-BR   : *PT
  pt-PT   : *PT
  en      : &EN       About
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
show_title: false
mode: immersive
header:
  theme: dark
article_header:
  type: overlay
  theme: dark
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87, .4), rgba(139, 34, 139, .4))'
    src: /assets/images/louis-reed-zDxlNcdUzxk-unsplash.jpg
    reference: '<span>Photo by <a href="https://unsplash.com/@_louisreed?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Louis Reed</a> on <a href="https://unsplash.com/s/photos/raspberry-pi?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>'
key: page-about
---
{%- if page.article_header.background_image.reference -%}
<div style="text-align: center">
  {{ page.article_header.background_image.reference }}
</div>
{%- endif -%}

{%- if page.i18n_title -%}
  <h1>{%- translate page.i18n_title -%}</h1>
{%- endif -%}

{%- if site.lang == "pt" -%}
  {%- capture link1 -%}{{ site.baseurl_root }}/en{{ page.url}}{%- endcapture -%}
  <strong>{%- translate texts.read_on -%}: </strong><a href="{{ link1 }}" >{%- translate langs.english -%}</a>
{%- elsif site.lang == "en" -%}
  {%- capture link2 -%}{{ site.baseurl_root }}{{ page.url  }}{%- endcapture -%}
  <strong>{%- translate texts.read_on -%}: </strong><a href="{{ link2 }}" >{%- translate langs.portuguese -%}</a>
{%- endif -%}

</p>

{%- translate_file about.md -%}
