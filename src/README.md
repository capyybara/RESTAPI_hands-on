# REST API ハンズオン

第7回課題に関係して、課題に取り組む前にハンズオンをやってみました。<br>
以下に、リクエストごとに実行できたものの写真などを掲載しています。

<br><br>

## GETリクエスト

- curl＆ターミナルより

![REST API GET curl全体 2023-08-01 14 13 38](https://github.com/capyybara/RESTAPI_hands-on/assets/137416338/fbd53e3d-c72e-4af1-adb0-88f405d96d7d)

<br>
<br>

- Postmanより
<br>

<img width="877" alt="Postman GETリクエスト" src="https://github.com/capyybara/RESTAPI_hands-on/assets/137416338/9cf6fcc7-5287-413c-9087-8a2959235ffd">

<br>
<br>

## POSTリクエスト

<br>

- curl & ターミナルより

```
curl -i -H "Authorization: token github_pat_1cCEG0Ml3E1〜" \
>     -d '{
>         "name": "blog",
>         "auto_init": true,
>         "private": true,
>         "gitignore_template": "Nanoc"
>       }' \
>     https://api.github.com/user/repos
HTTP/2 201 
server: GitHub.com
date: Thu, 03 Aug 2023 05:07:25 GMT
content-type: application/json; charset=utf-8
content-length: 5700
cache-control: private, max-age=60, s-maxage=60
vary: Accept, Authorization, Cookie, X-GitHub-OTP

```

<br>

- Postmanより
<br>
  <img width="839" alt="POSTリクエスト Postman" src="https://github.com/capyybara/RESTAPI_hands-on/assets/137416338/eab6cf55-f225-4bb7-acb7-001aebb2e8d5">


<br>
<br>


##  PATCHリクエスト

![PATCHリクエストURL](https://github.com/capyybara/RESTAPI_hands-on/assets/137416338/628caf2e-8c03-4bf2-9253-3e82496fe80b)


```

curl -i -X PATCH \
  -H "Accept: application/vnd.github.v3+json" \
  -H "Authorization: token github_pat_11BYM5l3E~" \
  https://api.github.com/repos/capyybara/blog \
  -d '{
    "name":"hello-world-blog",
    "description":"This is your blog repository",
    "homepage":"https://github.com",
    "private":false
  }'

HTTP/2 200 
server: GitHub.com
date: Thu, 03 Aug 2023 06:04:05 GMT
content-type: application/json; charset=utf-8



```

