# Shop-by-Node.js
Node.js를 이용해서 만든 Shop

#### https://desolate-earth-51883.herokuapp.com/ 에서 직접 사용해볼 수 있다.


## 기능 (표시된 것들은 구현 성공)
 - [X] Shop 서버의 기본 틀.
 - [X] Add Product
 - [ ] Edit Product
 - [ ] Delete Product
 - [ ] MySQL DB
 - [ ] Cart Page
 - [ ] Order Page
 - [ ] Login
 - [ ] Mongo DB
 - [ ] .... (프로젝트 진행하며 필요한 것들 추가)


## Heroku 업로드 팁
 - [여기](https://medium.com/@yoobi55/express-node-js-%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%B4-%EC%84%9C%EB%B2%84%EB%A5%BC-%EB%A7%8C%EB%93%A4%EC%96%B4-heroku%EC%97%90-%EC%98%AC%EB%A6%AC%EB%8A%94-%EB%B0%A9%EB%B2%95-3a5134fc8743 "express/node.js 를 이용해 서버를 만들어 heroku에 올리는 방법") 나 [여기](https://unikys.tistory.com/317 "[Nodejs] 무료 호스팅 서버 Heroku 사용하기/소스 올리기 (윈도우)") 참고

 1. Heroku에서 이용하는 포트로 바꿔주기
 ```
 const PORT = process.env.PORT
 app.listen(PORT)
 ```
 
 2. package.json 파일 수정
 ```
 "engines":{
    "node": //노드 버젼 여기다 쓰세요 ,
    "npm": //엠피엠 버젼 여기다 쓰세요
 }
 ```
 ```
 “scripts” 에 “start”: “node index.js” 추가하기
 ```
 
 3. .gitignore 파일 추가
 
 .gitignore 파일에 아래 단어만 써서 추가. (여기서는 이렇게만 진행했지만 필요시 더 추가해서 사용)
 ```
 node_modules
 ```
 
 4. git
 
 ```
 git init 
 git add . 
 git commit -m "init heroku"
```

5. Heroku
```
heroku login
heroku create
git push heroku master
```

heroku create시에 나오는 주소가 해당 앱 주소.
주소 이름 임의로 정하고 싶으면 따로 앱 만들어서 해당 앱으로 푸시해서 진행.
