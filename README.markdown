# RestSharp - Simple REST Client for Unity3D

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
