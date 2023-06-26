---
layout: page
title: API Management
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
  {% for items in site.data.api-management %}
  {% if  items.services.size == 1 %}
   <tr>
    <td>{{items.concept}}</td>
    <td><a href="{{items.services.first.aws-url}}">{{items.services.first.aws}}</a></td>
    <td><a href="{{items.services.first.azure-url}}">{{items.services.first.azure}}</a></td>
    <td><a href="{{items.services.first.gcp-url}}">{{items.services.first.gcp}}</a></td>
   </tr>
  {% else %}
   <tr>
    <td rowspan="{{items.services.size}}">{{items.concept}}</td>
    <td style="text-align: center; vertical-align: middle;"><a href="{{items.services.first.aws-url}}">{{items.services.first.aws}}</a></td>
    <td style="text-align: center; vertical-align: middle;"><a href="{{items.services.first.azure-url}}">{{items.services.first.azure}}</a></td>
    <td style="text-align: center; vertical-align: middle;"><a href="{{items.services.first.gcp-url}}">{{items.services.first.gcp}}</a></td>
   </tr>
  {% for service in items.services offset:1 %}
   <tr>
    <td style="text-align: center; vertical-align: middle;"><a href="{{service.aws-url}}">{{service.aws}}</a></td>
    <td style="text-align: center; vertical-align: middle;"><a href="{{service.azure-url}}">{{service.azure}}</a></td>
    <td style="text-align: center; vertical-align: middle;"><a href="{{service.gcp-url}}">{{service.gcp}}</a></td>
   </tr>
  {% endfor %}
  {% endif %}
  {% endfor %}
 </tbody>
</table>
