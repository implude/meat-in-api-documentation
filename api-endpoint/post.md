# 포스트 \(/post\)

```text
Comment {
    "title": String,
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

{% api-method method="get" host="" path="/post/curated" %}
{% api-method-summary %}
Get Curated Post
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
BriefPost[]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/post/:id" %}
{% api-method-summary %}
Get Specific Post
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Post
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="" path="/post" %}
{% api-method-summary %}
Create Post
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="linked\_recipe" type="string" required=true %}
Recipe Id
{% endapi-method-parameter %}

{% api-method-parameter name="content" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="photo" type="string" required=true %}
base64 encoded image
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Post
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/post/:id/comment" %}
{% api-method-summary %}
Create Comment
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="content" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

