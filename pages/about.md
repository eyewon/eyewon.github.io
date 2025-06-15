---
layout: default
title: About
permalink: /about
weight: 0
---

<style>
span#label {
  font-size: 80% !important;
}
#title-list {
  /* opacity: 0.5; */
  text-align: right;
  a {
    text-decoration: none;
    font-weight: bold;
  }
}
.alert.alert-light {
  border-color: #e9ecef !important;
  color: #495057 !important;
  background-color: #fcfcfd !important;
}
@media only screen and (min-width: 1088px) {
  #title-list {
    /* writing-mode: vertical-rl; */
    /* transform: rotate(180deg); */
    position: fixed;
    top: 200px;
    right: 22px;
  }
}
</style>

<div class="mx-auto mt-5 px-5">
  <div class="markdown-body">
    <h3>안녕하세요✨</h3>
    <h1 style="margin-top: 0px;">이예원입니다</h1>
    <p>
      <div>모든 프로젝트의 시작과 끝을 '사용자 경험'에 두는 개발자,</div>
      <div>사용자의 불편을 발견하고, 공감하며, 함께 성장한느 서비슬르 만듭니다.</div>
    </p>
    <p class="mb-2">
      <span class="badge badge-pill text-primary border border-primary mr-2" id="label">Email</span>
      eye_o-o@naver.com
    </p>
    <p class="mb-2">
      <span class="badge badge-pill text-primary border border-primary mr-2" id="label">Github</span>
      <a href="https://github.com/eyewon" target="_blank">github.com/eyeon</a>
    </p>
    <p class="mb-2">
      <span class="badge badge-pill text-primary border border-primary mr-2" id="label">Blog</span>
      <a href="https://yes-im-on.tistory.com/" target="_blank">yes-im-on.tistory.com</a>
    </p>
    <h2 id="programming-skills" class="mt-5 mb-2">Programming Skills</h2>
    <div class="row">
      {% include about/skills.html title="Language" star="0,1,2" source=site.data.skills.language %}
      {% include about/skills.html title="Web Framework" star="0" source=site.data.skills.framework %}
      {% include about/skills.html title="Database" star="0,1" source=site.data.skills.database %}
    </div>
    <h4 class="mt-3 mb-3">Tools</h4>
    <div class="row">
        {% for skill in site.data.skills.tool %}
        <div class="col-lg">
          <div class="alert alert-{{ skill.color | default: "primary" }}" role="alert">
            <div class="d-flex flex-row justify-content-start align-items-center">
              <p class="mb-1 mr-2"><b>{{ skill.name }}</b></p>
              <div style="font-size: small;">
                {{ skill.explain }}
              </div>
            </div>
          </div>
        </div>
        {% endfor %}
    </div>
    
    <h2 id="projects">Projects</h2>
  </div>

  <div class="row">
  {% include projects/index.html %}
  </div>

  <div class="markdown-body">
    <h2 id="education">Education</h2>
    <div class="row">
    {% include about/education.html %}
    </div>

    <h2 id="certificate">Certificate</h2>
    <div class="row">
    {% include about/certificate.html %}
    </div>

    <h2 id="awards">Awards</h2>
    <div class="row">
    {% include about/awards.html %}
    </div>

    <h2 id="activities">Activities</h2>
    <div class="row">
    {% include about/activity.html %}
    </div>
    
    <footer class="mt-auto py-3 text-center">
      <small id="title-list">
        <a href="#programming-skills">Skills</a><br>
        <a href="#projects">Projects</a><br>
        <a href="#experience">Experience</a><br>
        <a href="#education">Education</a><br>
        <a href="#certificate">Certificate</a><br>
        <a href="#awards">Awards</a><br>
        <a href="#activities">Activities</a>
      </small>
    </footer>
  </div>
</div>