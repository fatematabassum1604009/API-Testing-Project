# API-Testing-Project
Performed API testing on frequently used API for a test site [Testing World API](https://thetestingworldapi.com). This project provides an example for testing APIs with Postman.<br>
<b><h3>Why use Postman?</h3></b>
Postman is a popular and easy-to-use API testing tool. It is simple to build & send requests and examine the responses, making it popular for exploratory and manual testing of APIs. However, Postman is capable of much more and is often overlooked as an automated API testing tool.<br>
<b><h3>Postman Test Suite</h3></b>
The Postman test suite here is made up of two separate files:
<ul>
<li>Fatema_Tabassum_21.postman_collection.json</li>
<li>Fatema_Tabassum_21.postman_environment.json</li>
</ul>
The first file is the Postman collection - this contains all the individual requests and tests. The second file is the Postman environment - this contains a set of variables that can be used in postman requests.<br>
<b><h3>Postman Collection</h3></b>
The Postman collection is a JSON structure containing all the API requests and the associated tests. The collection itself is hierarchical with three main components:
<ul>
<li>collection</li>
<li>folders (and sub-folders)</li>
<li>requests</li>
</ul>
Each level in this hierarchy supports pre-request scripts and tests. Both are points at which JavaScript code can be entered with pre-request scripts run before the request is sent (as the name suggests) and tests run afterwards. We can exploit both of these to help with our tests.<br>
<b><h3>Postman Environment</h3></b>
Environment files are a quick way of switching between different configurations such as test and production. They are also handy for storing variables (see below). These may be variables that may vary between environments (e.g. the base API URL) or 'temporary' variables that are declared in pre-request scripts, with the tests then reading those variables for use in assertions.<br>
<b><h3>Variables</h3></b>
Postman collections and environments support the declaration and storage of variables. These are available to all requests and any code within the collection, but are not accessible outside the collection. In this case we have six variables defined at the environment file:
<ul>
<li>Base_Url = https://thetestingworldapi.com</li>
<li>first_name</li>
<li>middle_name</li>
<li>last_name</li>
<li>date_of_birth</li>
<li>id</li>
</ul>
<b><h3>Tests</h3></b>
For each request, we generally run the following tests:
<ul>
<li>response is received in a timely manner</li>
<li>response has the right status code</li>
<li>response is in the correct format (e.g JSON)</li>
<li>response schema is correct</li>
<li>response body contents are correct</li>
 </ul>
<b><h3>What is Newman?</h3></b>
Newman is a command-line Collection Runner for Postman. It enables you to run and test a Postman Collection directly from the command line.<br>
<b><h3>To run this project:</h3></b>
<ul>
<li>Clone this project.</li>
<li>Open with Postman / Command Shell.</li>
<li>Command to run the project from the command prompt:</li>
 
 ```
newman run Fatema_Tabassum_21.postman_collection.json -e Fatema_Tabassum_21.postman_environment.json
 ```
 <li>Run this command for report:</li>
 
 ```
newman run Fatema_Tabassum_21.postman_collection.json -e Fatema_Tabassum_21.postman_environment.json -r cli,htmlextra
 ```
</ul>

<b><h3>API documentation</h3></b>
<ul>
<li>https://documenter.getpostman.com/view/13082503/2s93Xwz4Az</li>
</ul>
<b><h3>Newman Summary Report Screenshot:</h3></b><br>

![report](https://github.com/fatematabassum1604009/API-Testing-Project/assets/34239300/4547079c-b85f-468a-89e1-33ed354891c3)
![report2](https://github.com/fatematabassum1604009/API-Testing-Project/assets/34239300/1e8820cc-9ffa-43c0-a3bc-0dc6b2f44c5a)


