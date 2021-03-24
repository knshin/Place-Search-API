# Place-Search-API
Place search API practice

<회원가입>
curl -d@create-user.json -H "Content-Type: application/json" -X POST http://localhost:8080/account/v1/user

[create-user.json]
{
	"name":"honggildong",
	"password":"test test"
}

<로그인>
curl -d@login-user.json -H "Content-Type: application/json" -X POST http://localhost:8080/account/v1/login

[login-user.json]
{
	"name":"honggildong",
	"password":"test test"
}

<장소검색>
curl -H "Content-Type: application/json" -X GET http://localhost:8080/place/v1/search?query=starbucks

<내검색 히스토리>
curl -H "Content-Type: application/json" -X GET http://localhost:8080/place/v1/search/history

<인기 키워드 목록>
curl -H "Content-Type: application/json" -X GET http://localhost:8080/place/v1/search/popularity
