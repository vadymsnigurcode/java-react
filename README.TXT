Resource:
https://www.baeldung.com/spring-boot-react-crud

Create react project steps:

npx create-react-app frontend

npm install --save bootstrap@5.1 react-cookie@4.1.1 react-router-dom@5.3.0 reactstrap@8.10.0

Let's add Bootstrap's CSS file as an import in app/src/index.js:
import 'bootstrap/dist/css/bootstrap.min.css';

npm start

For that, we'll include the URL for our API in package.json:
...
"proxy": "http://localhost:8080",
...



Add data cmd:
curl -i -X POST localhost:8080/clients -d "{\"name\":\"John Doe\", \"email\":\"john.doe@baeldgung.com\"}" -H "Content-Type:application/json"