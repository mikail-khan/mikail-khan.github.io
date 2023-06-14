---
layout: page
title: AI & Machine Learning
---

<table>
 <thead>
  <tr>
   <th>Concept</th>
   <th>AWS</th>
   <th>Azure</th>
   <th>GCP</th>
  </tr>
 </thead>
 <tbody>
  {% for member in site.data.ai-ml %}
  <tr>
   <td>{{member.concept}}</td>
   <td><a href="{{member.aws-url}}">{{member.aws}}</a></td>
   <td><a href="{{member.azure-url}}">{{member.azure}}</a></td>
   <td><a href="{{member.gcp-url}}">{{member.gcp}}</a></td>
  </tr>
  {% endfor %}
 </tbody>
</table>
