---
layout: post
title: Artificial Intelligence & Machine Learning
---

AI & ML services and products across the three main cloud providers
can essentially be grouped into four main categories:

1. **Machine Learning as a Service**: unified platforms for building,
training, and deploying AI/ML models,
2. **AI Infrastructure**: Dedicated hardware to develop and run AI workloads,
3. **AI for Developers**: Machine Learning SaaS and APIs which
developers can integrate into their applications to build AI services
and applications,
4. **Managed AI Solutions**: Predefined managed AI solutions for
   industry applications.

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
  {% for items in site.data.ai-ml %}
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


