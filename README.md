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

<Endpoint에 대한 부하가 매우 커졌을 경우 확장 방안>
API구현체에서 Cache를 이용하여 특정 기간 동안 이미 조회한 검색어는 Cache에서 서비스,
End Point에 부하 최소화

<추가적으로 사용한 오픈소스>
json - JSON 파싱용
Apache Codec - 사용자 패스워드 해시값 생성용
ehcache - 검색 결과 캐싱용
