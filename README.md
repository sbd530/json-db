## Node.js Json DB

### Installation

```shell
npm install
```

### Unit Test

```shell
npm run test
```

### Requirements

1. 사용자에게 입력을 받아 과일에 대한 정보를 조회합니다. 과일 하나당 하나의 레코드(이름과 원산지)를 가지며, 레코드는 식별자로써 0 이상의 정수형인 `_id` 를 가집니다.

```json
{
  "_id": 0,
  "name": "apple",
  "origins": [
    { "origin": "korea", "price": 1000 },
    { "origin": "japan", "price": 2000 }
  ]
}
```

2. 프로그램을 실행 시켰을 때 사용자에게 유저 아이디와 패스워드를 입력 받고, `.env`에 저장된 userid와 password의 값과 일치하지 않으면 프로그램을 종료합니다.

3. 로그인에 성공하면, 쿼리를 입력받습니다:

- 조회 쿼리 예

```shell
$ find apple

{
  "_id": 0,
  "name": "apple",
  "origins": [
    { "origin": "korea", "price": 1000 },
    { "origin": "japan", "price": 2000 }
  ]
}
```

```shell
$ find like *ppl*

{
  "_id": 0,
  "name": "apple",
  "origins": [
    { "origin": "korea", "price": 1000 },
    { "origin": "japan", "price": 2000 }
  ]
},
{
  "_id": 13,
  "name": "pineapple",
  "origins": [
    { "origin": "philippines", "price": 6000 },
    { "origin": "vietnam", "price": 5000 }
  ]
}
```

```shell
$ find --all

{
  "_id": 0,
  "name": "apple",
  "origins": [
    { "origin": "korea", "price": 1000 },
    { "origin": "japan", "price": 2000 }
  ]
},
{
  "_id": 1,
  "name": "orange",
  "origins": [
    { "origin": "usa", "price": 2000 },
    { "origin": "australia", "price": 3000 }
  ]
},
...
```

```shell
$ find grape

No such fruit.
```

```shell
$ findsomething
$ find
$ find--all

Wrong Grammer.
```

- 삭제 쿼리 예

```shell
$ delete apple
apple deleted.

$ delete grape
No such fruit.

$ delete --all
All of data has been deleted.

$ delete
$ deleteapple
$ delete--all

Wrong Grammer.
```

5. `exit` 명령어를 받으면 프로그램을 종료합니다.

```shell
$ exit
See ya.
```
