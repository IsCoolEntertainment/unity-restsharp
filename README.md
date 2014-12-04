# RestSharp - Simple REST Client for Unity3D

Reduced version of original RestSharp client (no authentication for the moment, for instance).
Some of the RestSharp APIs were based on .NET natives.

This current reduced version works with UnityEngine and its mono system libs.

Originally written by [restsharp team](https://github.com/restsharp/RestSharp).
Based on [Cratesmith](https://github.com/Cratesmith/RestSharp-for-unity3d) fork.

## Working example

```csharp
var client = new RestClient("http://example.com/api");

// Create a new post request on http://example.com/api/books
var request = new RestRequest("books", Method.POST);

// adds to POST or URL querystring based on Method
request.AddParameter("name", "value");

client.ExecuteAsync(request, response => {
    print(response.Content);
});
```
