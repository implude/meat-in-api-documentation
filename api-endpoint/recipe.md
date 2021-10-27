# 레시피 (/recipe)

```
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

{% swagger baseUrl="" path="/recipe/curated" method="get" summary="Get Curated Recipe" %}
{% swagger-description %}
레시피 목록을 반환합니다
{% endswagger-description %}

{% swagger-response status="200" description="Cake successfully retrieved." %}
```
BriefRecipe[]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/recipe/:id" method="get" summary="Get Specific Recipe" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
Recipe
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/recipe/:id/step" method="get" summary="Get Recipe Steps" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
RecipeStep[]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/recipe" method="post" summary="Create Recipe" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="ingredient" type="array" required="true" %}
Ingredient[]
{% endswagger-parameter %}

{% swagger-parameter in="body" name="youtube" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="difficulty" type="number" required="true" %}
Difficulty List에서 받아온 난이도를 숫자로 입력해주세요
{% endswagger-parameter %}

{% swagger-parameter in="body" name="duration" type="string" required="true" %}
조리시간을 초단위로 입력해주세요
{% endswagger-parameter %}

{% swagger-parameter in="body" name="description" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="thumbnail" type="string" required="true" %}
Base64 encoded image
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
Recipe
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/recipe/difficulty" method="get" summary="Get Difficulty Lists" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200" description="" %}
```
Difficulty[]
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/recipe/:id/heart" baseUrl="" summary="Heart Recipe" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" required="true" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="get" path="/recipe/:id/bookmark" baseUrl="" summary="Bookmark Post" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" required="true" %}

{% endswagger-parameter %}
{% endswagger %}
