# 레시피 \(/recipe\)

```text
BriefRecipe {
  "name": String,
  "thumbnail": String,
  "meat_type": MeatType,
  "duration": Number,
  "difficulty": Difficulty,
  "created_at": Timestamp,
  "heart": Heart
}

Recipe {
  "thumbnail": String,
  "name": String,
  "created_at": Timestamp,
  "description": String,
  "author": BriefCommunityUser,
  "duration": Number,
  "difficulty": Difficulty,
  "heart": Heart,
  "youtube": String,
  "ingredient": Ingredient[],
  "brief_content": String[],
  "linked_post": BriefPost[]
}

RecipeStep {
  "image": String,
  "title": String,
  "content": String
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

{% api-method method="get" host="" path="/recipe/:id/step" %}
{% api-method-summary %}
Get Recipe Steps
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
RecipeStep[]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="" path="/recipe" %}
{% api-method-summary %}
Create Recipe
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="ingredient" type="array" required=false %}
Ingredient\[\]
{% endapi-method-parameter %}

{% api-method-parameter name="youtube" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="difficulty" type="number" required=true %}
Difficulty List에서 받아온 난이도를 숫자로 입력해주세요
{% endapi-method-parameter %}

{% api-method-parameter name="duration" type="string" required=true %}
조리시간을 초단위로 입력해주세요
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="thumbnail" type="string" required=true %}
Base64 encoded image
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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

{% api-method method="get" host="" path="/recipe/difficulty" %}
{% api-method-summary %}
Get Difficulty Lists
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
Difficulty[]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

