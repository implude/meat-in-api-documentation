---
description: 사용자 인증에 관련된 라우트
---

# 사용자 (/user)

```
BriefCommunityUser = Me {
  "name": String,
  "photo": String,
  "rep_badge": BriefBadge,
}

CommunityUser {
  "name": String,
  "rep_badge": BriefBadge,
  "badge_list": Badge[],
  "uploaded_post": BriefPost[],
  "uploaded_recipe": BriefRecipe[]
}

User {
  "email": String,
  "name": String,
  "photo": String
}
```

{% swagger baseUrl="" path="/user/me" method="get" summary="Get my info" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="Authorization" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
Me
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/user/me" method="patch" summary="Modify My Info" %}
{% swagger-description %}
This endpoint allows you to get free cakes.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="email" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="image" type="string" %}
Encode profile image with base64
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
Me
```
{% endswagger-response %}

{% swagger-response status="400" description="올바르지 않은 업데이트 데이터입니다" %}
```
{
    "error": "FIELD_VALIDATION_FAILED"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/user/:id" method="get" summary="Get Community User" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
CommunityUser
```
{% endswagger-response %}
{% endswagger %}
