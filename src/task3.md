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

```typescript
// <Write your code here, feel free to change language if you prefer>
```

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

```typescript
// <Write your code here, feel free to change language if you prefer>
```

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

```typescript
// <Write your code here, feel free to change language if you prefer>
```
    
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

```typescript
// <Write your code here, feel free to change language if you prefer>
```