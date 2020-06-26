# helloSpringBoot-Product
# 웹프레임워크2[B] - 과제 3
> # 1592029 정지성
<br>

***

* # Spring Boot를 활용하여 Product에 대한<br>CRUD 메소드를 제공하는 REST API를 구현하라.
<br>

***

* ## 테이블 구조 및 생성 결과
> ![db](https://user-images.githubusercontent.com/52397000/85845171-d1e09300-b7de-11ea-99fa-9ad0f978044c.PNG)
> * 첫 실행시 자동 생성되는 테이블입니다.

***

* ## API Method 실행 과정 및 결과
> ### 1. Get full list of products: http://localhost:9090/api/v1/products
> ![GetProducts1](https://user-images.githubusercontent.com/52397000/85845648-88447800-b7df-11ea-8ab5-a7f30ec481a1.PNG)
> ![GetProducts2](https://user-images.githubusercontent.com/52397000/85845667-92ff0d00-b7df-11ea-9022-cfae06f29d5f.PNG)
> * Get 메소드를 사용하여 products 테이블의 모든 데이터를 출력하였습니다.
> * 첫 실행 후 자동 생성되는 DB 데이터로 위 테이블 구조 이미지와 동일한 구성인 것을 확인할 수 있습니다.

> ### 2. Get details of products with id=N: http://localhost:9090/api/v1/products/{id}
> ![GetProducts-id](https://user-images.githubusercontent.com/52397000/85846409-be362c00-b7e0-11ea-8ee9-7c56e1d0ea67.PNG)
> * id = 6인 데이터를 조회하였습니다.

> ### 3. Fetch all products of a category: http://localhost:9090/api/v1/products/category/{category}
> ![GetProducts-category](https://user-images.githubusercontent.com/52397000/85846494-dc039100-b7e0-11ea-86b3-fea939544e72.PNG)
> * category = Computer인 데이터를 모두 조회하였습니다.

> ### 4. Update (PUT): modify values of product with id=N: http://localhost: 9090/api/v1/products/{id}
> ![Put](https://user-images.githubusercontent.com/52397000/85846691-284ed100-b7e1-11ea-970a-8624fb970c7e.PNG) 
> * Put 메소드를 이용해 id=3의 데이터의 price와 description을 수정하였습니다.

> ### 5. Delete (DELETE): delete product with id=N: http://localhost:9090/api/v1/products/{id}
> ![Delete1](https://user-images.githubusercontent.com/52397000/85847146-ebcfa500-b7e1-11ea-9340-9cf3c3c49cb6.PNG)
> * DELETE 메소드를 이용해 id = 1인 데이터를 삭제하였습니다.
> ![Delete2](https://user-images.githubusercontent.com/52397000/85847150-ed00d200-b7e1-11ea-8fde-b4e1de7a36bd.PNG)
> * DELETE 후 결과입니다. id = 1인 데이터가 삭제된 것을 확인할 수 있습니다.

> ### 6. Create/Add(POST): create new product: http://localhost:9090/api/v1/products
> ![Post](https://user-images.githubusercontent.com/52397000/85847463-5ed91b80-b7e2-11ea-9a6b-e7aeef3a2697.PNG)
> * 마지막으로 POST 메소드를 이용해 새로운 데이터를 추가하였습니다.

***

<br>

* ## Spring Boot의 acuator를 활용하여<br> Products REST API에 대한 URL Mapping 정보 캡쳐 결과
> ### app info 정보 http://localhost:9090/actuator/info
> ![info](https://user-images.githubusercontent.com/52397000/85849202-7e257800-b7e5-11ea-9fbc-95403b0feff6.PNG)
> * application.properties에서 설정한 info 내용입니다.

> ### mappings 정보 http://localhost:9090/actuator/mappings
> ![rawmapping](https://user-images.githubusercontent.com/52397000/85847917-3bfb3700-b7e3-11ea-94c2-7f187fa80fc0.PNG)
> * mappings의 모든 정보 출력 화면입니다. (raw)

> ### 1. GET Method: getAllProducts(), getProductById(int), findByCategory(String)
> ![getAllProducts](https://user-images.githubusercontent.com/52397000/85848176-af9d4400-b7e3-11ea-87b4-44e5abe3d277.PNG)
> * getAllProducts()

> ![getProductById](https://user-images.githubusercontent.com/52397000/85848217-c2177d80-b7e3-11ea-913a-3ad64fcde477.PNG)
> * getProductById(int)

> ![findByCategory](https://user-images.githubusercontent.com/52397000/85848224-c3e14100-b7e3-11ea-800f-49374a3f7875.PNG)
> * findByCategory(String)

> ### 2. PUT Method: updateProduct(int, Product)
> ![updateProduct](https://user-images.githubusercontent.com/52397000/85848518-3baf6b80-b7e4-11ea-809e-f5a6050de26c.PNG)
> * updateProduct(int, Product)

> ### 3. DELETE Method: deleteProduct(int)
> ![deleteProduct](https://user-images.githubusercontent.com/52397000/85848742-a06ac600-b7e4-11ea-9d1d-316588ae0d59.PNG)
> * deleteProduct(int)

> ### 4. POST Method: postProduct(Product)
> ![postProducts](https://user-images.githubusercontent.com/52397000/85848817-c7c19300-b7e4-11ea-8c45-1baa8bab12d4.PNG)
> * postProducts(Product)

***
