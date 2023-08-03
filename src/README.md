# REST API ハンズオン

第7回課題に関係して、課題に取り組む前にハンズオンをやってみました。<br>
以下に、リクエストごとに実行できたものの写真などを掲載しています。

## GETリクエスト

- curl＆ターミナルより

<img width="635" alt="APIハンズオン GETリクエスト" src="https://github.com/capyybara/RESTAPI_hands-on/assets/137416338/4c7609f6-6b51-44b9-8d82-5af1f351116b">

- Postmanより
<br>

<img width="877" alt="Postman GETリクエスト" src="https://github.com/capyybara/RESTAPI_hands-on/assets/137416338/9cf6fcc7-5287-413c-9087-8a2959235ffd">

<br>

## POSTリクエスト

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

なぜか、Postmanでは　（blog02でも）エラーが出たため実行できませんでした…💦
<br>
<br>

##  PATCHリクエスト

![PATCHリクエストURL](https://github.com/capyybara/RESTAPI_hands-on/assets/137416338/628caf2e-8c03-4bf2-9253-3e82496fe80b)

