API 명세서
------
|속성|Method|URL|request|response|status code|
|------|---|---|---|---|---|
|일정 생성|POST|/api/schedule|요청 body|일정 등록 정보|200: 정상 등록|
|전체 일정 조회|GET|/api/schedule|요청 param|다건 응답 정보|200: 정상 조회|
|선택 일정 조회|GET|/api/schedule{scheduleId}|요청 param|단건 응답 정보|200: 정상 조회|
|선택 일정 수정|PUT|/api/schedule{scheduleId}|요청 body|수정 정보|200: 정상 수정|
|선택 일정 삭제|DELETE|/api/schedule{scheduleId}|요청 param|-|200: 정상 삭제|

ERD
------
![ERD](https://github.com/user-attachments/assets/c61d9169-34aa-430c-9577-ed2b1b3b612b)

https://www.erdcloud.com/d/WfodqEtyJB6D663po

SQL
------
