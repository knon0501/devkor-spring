# REST API 설계

SCPC는 난이도 정보를 찾기 힘들어서 솔브드처럼 SCPC에 출제된 문제들의 난이도 정보를 보여주는 웹서비스를 생각해 보았습니다.



| METHOD | URI                      | Params    | Body                             | Description                                                  |
| ------ | ------------------------ | --------- | :------------------------------- | ------------------------------------------------------------ |
| GET    | :/difficulty/{id,subnum} | id,subnum |                                  | 특정 문제의 특정 서브태스크 난이도 조회                      |
| POST   | :/difficulty/{id,subnum} | id,subnum | comment,difficulty               | 특정 문제의 특정 서브태스크 난이도 투표                      |
| POST   | :/problem                |           | year,competition,num,subcnt,link | 년도,예선본선여부,문제번호,서브태스크 개수,문제url 의 정보를 가지는 문제 추가 |
| PUT    | :/problem/{id}           | id        | year,competition,num,subcnt,link | 특정 문제의 정보를 수정                                      |
| DELETE | :/problem/{id}           |           |                                  | 특정 문제를 삭제                                             |
| DELETE | :/difficulty/{id,subum}  | id,subnum |                                  | 특정 문제의 특정 서브태스크의 난이도투표를 전부 삭제D        |
| PUT    | :/difficulty/vote/{id}   | id        | comment,difficulty               | 특정 투표를 수정                                             |
| DELETE | :/difficulty/vote/{id}   | id        |                                  | 특정 투표를 삭제                                             |

