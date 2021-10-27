# 포스트 (/post)

```
Comment {
    "created_at": Timestamp,
    "author": BriefCommunityUser,
    "content": String,
}

Post {
    "photo": String[],
    "title": String,
    "created_at": Timestamp,
    "author": BriefCommunityUser,
    "content": String,
    "linked_recipe": BriefRecipe,
    "comment": Comment[],
    "heart": Heart,
    "bookmarked": Boolean
}

BriefPost {
  "author": BriefCommunityUser,
  "created_at": Timestamp,
  "heart": Heart,
  "comment_count": Number
}
```

{% swagger baseUrl="" path="/post/curated" method="get" summary="Get Curated Post" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200" description="" %}
```
BriefPost[]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/post/:id" method="get" summary="Get Specific Post" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
Post
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/post" method="post" summary="Create Post" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="linked_recipe" type="string" required="true" %}
Recipe Id
{% endswagger-parameter %}

{% swagger-parameter in="body" name="content" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="title" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="photo" type="string" %}
base64 encoded image
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
Post
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/post/:id/comment" method="post" summary="Create Comment" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="content" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
Comment
```
{% endswagger-response %}
{% endswagger %}
