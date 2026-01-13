---
title: 首頁
---

# 所有文章

{{ range where .Site.RegularPages "Section" "posts" }}
  <h2><a href="{{ .RelPermalink }}">{{ .Title }}</a></h2>
  <p><small>{{ .Date.Format "2006年1月2日" }}</small></p>
  <p>{{ .Summary | safeHTML }}</p>
  <hr>
{{ end }}