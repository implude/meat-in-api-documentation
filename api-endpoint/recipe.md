# 레시피 \(/recipe\)

```text
BriefRecipe {
  "name": String,
  "thumbnail": String,
  "meat_type": MeatType,
  "duration": Number,
  "difficulty": String,
  "created_at": Timestamp,
  "heart": Heart
}
```

```text
Recipe {
  "thumbnail": String,
  "name": String,
  "created_at": Timestamp,
  "description": String,
  "author": BriefCommunityUser,
  "duration": Number,
  "difficulty": String,
  "heart": Heart,
  "youtube": String,
  "ingredient": Ingredient[],
  "brief_content": String[],
  "linked_post": BriefPost[]
}
```

{% api-method method="get" host="" path="/recipe/curated" %}
{% api-method-summary %}
Get Curated Recipe
{% endapi-method-summary %}

{% api-method-description %}
레시피 목록을 반환합니다
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
BriefRecipe[]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/recipe/:id" %}
{% api-method-summary %}
Get Specific Recipe
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Recipe
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



