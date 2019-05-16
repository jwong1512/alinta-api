# alinta-api
A simple API relating to Customers of Alinta Energy

### Notes:
* The Api is written in ASP.NET Core 2.1. I have yet to use ASP.NET Core 2.2.

### Instructions on using the Api:
1. Clone the repository to your local computer.

1. Navigate to the **alinta-api\alintaApi\alintaApi.sln** file. Double click on the solution to open it in Visual Studio.

    ![Open the Alinta Solution](https://github.com/jwong1512/alinta-api/blob/master/Images/open_alinta-api_solution.gif)

1. In Visual Studio, run the application.

1. The Web Browser should appear that immediately navigates to **https://localhost:44333/api/customers** and displays the list of customers.

    ![Display Data in Browser](https://github.com/jwong1512/alinta-api/blob/master/Images/api_data.gif)

1. Use Postman to send your Requests.

    ![Postman Get Request](https://github.com/jwong1512/alinta-api/blob/master/Images/postman_get_request.gif)

## Swagger Instructions

1. In Visual Studio, run the Api.

1. Navigate to the following Url to get all the Swagger metadata: 
**https://localhost:44333//swagger/v1/swagger.json**
1. Navigate to the following Url to use the Swagger UI: 
**https://localhost:44333//swagger/index.html**

## Instructions on Sending Requests

### GET Request

* There is only one parameter in the GET Request and that is the order in which you want to sort the data, in alphabetic order based on the customers First name.
* If no query string variable is passed through the Url then the GET Request sorts the Customers in order of how they appear in the Data Store.
* The following is an example of a GET 

    ![Get Request with querystring variable](https://github.com/jwong1512/alinta-api/blob/master/Images/get_request_with_querystring_variable.gif)

### GET Request with Id

* There is another GET Request that returns a customer based on the Id provided.
* The following is an example of a GET Request with Id.

    ![Get Request with Id](https://github.com/jwong1512/alinta-api/blob/master/Images/get_request_with_id.gif)

### POST Request

* The Post Request takes in a customer object.
* The fields required are the **Id**, **firstName**, **lastName** and **dateOfBirth**.
* The **dateOfBirth** field can be written as a string with the format *yyyy-MM-dd*.
* An example of a POST Request is the following:

    ![Post Request](https://github.com/jwong1512/alinta-api/blob/master/Images/post_request.gif)

### PUT Request

* The Put Request takes in 2 parameters, the **Id** and the new **Customer Object**.
* An example of the PUT Request is as follows:

    ![Put Request](https://github.com/jwong1512/alinta-api/blob/master/Images/put_request.gif)

### DELETE Request

* The Delete Request takes in 1 parameter, the **Id** of the customer you want to delete.
* Below is an example of a DELETE Request:

    ![Put Request](https://github.com/jwong1512/alinta-api/blob/master/Images/delete_request.gif)

### SearchByName Method

* The **SearchByName** method is the method used to locate a customer based on either their **First Name**, **Last Name** or **both**.
* The search criteria is passed through as query string variables in a GET Request.
* An example of executing the method in Postman is shown below:

    ![SearchByName Method](https://github.com/jwong1512/alinta-api/blob/master/Images/searchbyname_method.gif)
