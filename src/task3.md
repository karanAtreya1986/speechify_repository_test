# API Assessment
Your task is to describe and implement a test suite that validates core functionality of a RESTful API. You will need to write tests for three essential operations:

1. Write a test for a basic GET request that retrieves a collection of resources
2. Write a test for a parameterized GET request that fetches a specific resource
3. Write a test for a POST request that creates a new resource

You will be using the JSONPlaceholder API (https://jsonplaceholder.typicode.com) which provides a mock REST API for testing purposes.

Please describe your solution and implement it in the code blocks provided below. You may use any programming language or testing framework of your choice. No need to import any libraries, as your solution will be checked manually by our engineers.


## 1. GET Request
**Objective:** Test the retrieval of data from an API.

**Steps:**
- Send a GET request to the endpoint: `https://jsonplaceholder.typicode.com/posts`

**Verify the following:**
- Response status code is `200`
- Response contains a list of posts in JSON format
- The response body includes keys such as `userId`, `id`, `title`, and `body`

**Solution:**
<!-- <Write your solution description here> -->
First send the GET request with all needed headers and authorisations if any.
Then get the response. Grab the response.
Then validate the response as mentioned in the question.
We used Java rest assured framework. 
Rest assured library deals with this.
For assertions we use Hamcrest Matchers.

```typescript
// <Write your code here, feel free to change language if you prefer>
```
java

import io.restassured.RestAssured;
import io.restassured.response.Response;
import org.junit.jupiter.api.Test;

import static io.restassured.RestAssured.given;
import static org.hamcrest.Matchers.*;

public class GetPostsTest {

private static final String BASE_URL = "https://jsonplaceholder.typicode.com";

@Test
public void testGetPosts() {
    RestAssured.baseURI = BASE_URL;

 Response response =
            given()
            .when()
                .get("/posts")
            .then()
                // Verify status code
                .statusCode(200)
                // Verify response is JSON array
                .body("$", not(empty()))
                // Verify required keys exist in first post
                .body("[0].userId", notNullValue())
                .body("[0].id", notNullValue())
                .body("[0].title", notNullValue())
                .body("[0].body", notNullValue())
                .extract().response();

}
}


---

## 2. GET Request with Query Parameters  
**Objective:** Validate API behavior with query parameters.

**Steps:**
- Send a GET request to fetch a specific post: `https://jsonplaceholder.typicode.com/posts/1`

**Verify the following:**
- Status code is `200`
- Response body contains a single post with `id` = 1
- Validate the `title` and `body` fields are not null


**Solution:**
<!-- <Write your solution description here> -->
First send the GET request with all needed headers and authorisations if any.
Parameter will ?1 to get the post number 1.
Then get the response. Grab the response.
Then validate the response as mentioned in the question.
We used Java rest assured framework. 
Rest assured library deals with this.
For assertions we use Hamcrest Matchers.


```typescript
// <Write your code here, feel free to change language if you prefer>
```
java

import io.restassured.RestAssured;
import org.junit.jupiter.api.Test;

import static io.restassured.RestAssured.given;
import static org.hamcrest.Matchers.*;

public class GetPostByQueryParamTest {

private static final String BASE_URL = "https://jsonplaceholder.typicode.com";

 @Test
    public void testGetPostByIdQueryParam() {
        RestAssured.baseURI = BASE_URL;

  given()
            // Use query parameter ?id=1
            .queryParam("id", 1)
        .when()
            .get("/posts")
        .then()
            // Verify status code is 200
            .statusCode(200)
            //  Response is an array, so check first element
            .body("[0].id", equalTo(1))
            // Verify title is not null
            .body("[0].title", notNullValue())
            //  Verify body is not null
            .body("[0].body", notNullValue());
    }
}


---

## 3. POST Request
**Objective:** Test the creation of new data via an API.

**Steps:**
- Send a POST request to `https://jsonplaceholder.typicode.com/posts` with the following payload:
    - `{ "title": "Test Title", "body": "This is a test post.", "userId": 123 }`

**Verify the following:**
- Response status code is `201` (Created)
- Response body contains the sent payload along with an `id` field for the new post

**Solution:**
<!-- <Write your solution description here> -->
First send the POST request with all needed headers and authorisations if any.
Then send the body in the request.
Send the complete request.
Grab the response.
Validate the response as mentioned in question.
We used Java rest assured framework. 
Rest assured library deals with this.
For assertions we use Hamcrest Matchers.

```typescript
// <Write your code here, feel free to change language if you prefer>
```
java

import io.restassured.RestAssured;
import org.junit.jupiter.api.Test;

import static io.restassured.RestAssured.given;
import static org.hamcrest.Matchers.*;

public class CreatePostTest {

private static final String BASE_URL = "https://jsonplaceholder.typicode.com";

@Test
    public void testCreatePost() {
        RestAssured.baseURI = BASE_URL;

   // Define payload
        String requestBody = "{ \"title\": \"Test Title\", \"body\": \"This is a test post.\", \"userId\": 123 }";

  given()
            .header("Content-type", "application/json; charset=UTF-8")
            .body(requestBody)
        .when()
            .post("/posts")
        .then()
            // Verify response code
            .statusCode(201)
            // Verify response contains expected payload
            .body("title", equalTo("Test Title"))
            .body("body", equalTo("This is a test post."))
            .body("userId", equalTo(123))
            // Verify response includes an id
            .body("id", notNullValue());
    }
}

    
---

## 4. Negative Testing
**Objective:** Validate the API’s behavior with invalid requests.

**Steps:**
- Send a GET request to an invalid endpoint: `https://jsonplaceholder.typicode.com/posts/9999`

**Verify the following:**
- Status code is `404` (Not Found)
- Response body contains an appropriate error message or an empty response


**Solution:**
<!-- <Write your solution description here> -->
First send the GET request with all needed headers and authorisations if any.
Send the complete request with invalid endpoint.
Grab the response.
Validate the response as mentioned in question.
We used Java rest assured framework. 
Rest assured library deals with this.
For assertions we use Hamcrest Matchers.

```typescript
// <Write your code here, feel free to change language if you prefer>
```
java

import io.restassured.RestAssured;
import io.restassured.response.Response;
import org.junit.jupiter.api.Test;

import static io.restassured.RestAssured.given;
import static org.hamcrest.MatcherAssert.assertThat;
import static org.hamcrest.Matchers.*;

public class FlexibleNegativeGetPostTest {

private static final String BASE_URL = "https://jsonplaceholder.typicode.com";

@Test
    public void testInvalidPostIdFlexibleResponse() {
        RestAssured.baseURI = BASE_URL;

 Response response =
            given()
            .when()
                .get("/posts/9999")
            .then()
                .statusCode(404) //Verify status code
                .extract().response();

 String body = response.getBody().asString();

 if (body.isEmpty()) {
            // Case 1: No content
            System.out.println("Response is empty string");
            assertThat(body, equalTo(""));
        } else if (body.equals("{}")) {
            // Case 2: Empty object
            System.out.println("Response is empty JSON object");
            assertThat(body, equalTo("{}"));
        } else {
            // Case 3: JSON error message
            System.out.println("Response contains error message: " + body);
            assertThat(response.jsonPath().getString("error"), notNullValue());
            assertThat(response.jsonPath().getString("error").toLowerCase(), containsString("not found"));
        }
    }
}
