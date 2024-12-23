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
![ERD](https://github.com/user-attachments/assets/ff371578-e119-4136-a078-59d375559c69)


https://www.erdcloud.com/d/WfodqEtyJB6D663po

SQL
------
```sql

-- 앞서 만든 ERD 기반 테이블 생성

CREATE TABLE schedule(
    id INT(100) NOT NUll AUTO_INCREMENT, -- 새로운 행이 추가될때 자동으로 숫자 증가
    todo VARCHAR(100) NULL, -- 해당 colum 에 NULL 값을 허용하지 않는다.
    name VARCHAR(100) NULL,
    password VARCHAR(100) NULL,
    create_date DATETIME NULL,
    edit_date DATETIME NULL,
    PRIMARY KEY (id) -- 테이블 내에서 각각의 행을 고유하게 식별하는 id
    );

-- 일정 생성 (SQL 명령어 + 테이블 명 + (컬럼 명))
INSERT INTO schedule (todo, name, password, create_date, edit_date)


-- 전체 일정 조회 (*: 모든 열을 선택한다.)
SELECT * FROM schedule


-- 선택 일정 조회
SELECT * FROM schedule


-- 선택 일정 수정
UPDATE schedule


-- 선택 일정 삭제
DELETE FROM schedule

```
Spring 심화주차 과제
1. Web Application 객체 지향적으로 구현
2. BeanValidation 을 통한 객체의 유효성 검증
3. Cookie/Session과 Filter 활용
4. 인증/인가 구현
5. JPA 활용(중요!)
심화주차 과제는 숙련주차 과제 완성 후 만들기(매니저님께 상담 하였음)
```
