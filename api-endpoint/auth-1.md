# 인증 (/user)

{% swagger baseUrl="" path="/user" method="post" summary="Create User" %}
{% swagger-description %}
This endpoint allows you to get free cakes.
{% endswagger-description %}

{% swagger-parameter in="body" name="name" type="string" required="true" %}
사용자 이름
{% endswagger-parameter %}

{% swagger-parameter in="body" name="photo" type="string" required="true" %}
Base64 encoded Image
{% endswagger-parameter %}

{% swagger-parameter in="body" name="email" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="Cake successfully retrieved." %}
```
{
    "accessToken": String,
    "refreshToken": String
}
```
{% endswagger-response %}

{% swagger-response status="403" description="생성중인 Username이 이미 존재합니다" %}
```
{
    "error": "USERNAME_ALREADY_EXIST"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/user/login" method="post" summary="Login with Username and Password" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="password" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="username" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
    "accessToken": String,
    "refreshToken": String
}
```
{% endswagger-response %}

{% swagger-response status="400" description="Username과 Password이 일치하는 계정을 찾을 수 없습니다" %}
```
{
    "error": "ACCOUNT_NOT_MATCHED"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="" path="/user/login" method="post" summary="Login with refreshToken" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="refreshToken" type="string" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{
    "accessToken": String,
    "refreshToken": String
}
```
{% endswagger-response %}

{% swagger-response status="400" description="refreshToken이 올바르지 않습니다" %}
```
{
    "error": "TOKEN_NOT_CORRECT"
}
```
{% endswagger-response %}
{% endswagger %}
