---
layout: post
title: API Management
---

[Research](https://www.akamai.com/newsroom/press-release/state-of-the-internet-security-retail-attacks-and-api-traffic)
conducted by [Akamai](https://www.akamai.com) indicates that majority
of internet traffic is attributable to API calls indicating the
wide-scale adoption of API-first based architectures and the
increasing trend towards Digital Transformation. AWS, Azure, and GCP
provide comprehensive support for building, managing, securing, and
deploying APIs, but it is GCP which differentiates itself with
providing additional cloud API management options. For example, all
three cloud providers offer a fully managed platform responsible for
the complete API development lifecycle as well as guarantees around
scalability and reliability. However, GCP offers [API
Management](https://cloud.google.com/api-gateway) which is a
lightweight alternative to a fully managed API platform making it
ideal for entry level API architectures and strategies. In addition,
it offers [Cloud Endpoints](https://cloud.google.com/endpoints) which
enables the customer to have complete control over API management.

The API management solutions can be categorised into three groups:

1. **Fully Managed API Platform**: build, manage, deploy, and secure
APIs for **any** use case, environment, and scalability level.
2. **Basic Managed API Platform**: develop, deploy, secure, and manage
   APIs. Ideal for serverless back ends.
3. **Customer Managed API Gateway**: provide customer with full
   control over the complete API development, deployment, scaling, and
   securing of the API solution.

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
