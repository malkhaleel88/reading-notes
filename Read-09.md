# **WRRC and Java**

## **The HTTP Request Lifecycle**

![HTTP Cycle](https://miro.medium.com/max/1378/1*4SEvcz6KvyaqOqBpJABTBg.png)

**Step 1: Local Processing**

**Step 2: Resolve an IP**

**Step 3: Establish a TCP Connection**

**Step 4: Send an HTTP Request**

**Step 5: Tearing Down and Cleaning Up**

1. At first the browser need to convert the (www.example.com) to an *IP address* if it does not already know it. If it knows it, nothing happens at this point. If it does not know it, it contacts a DNS server to resolve the name.

2. Then browser will open a TCP connection to the IP address of 9www.example.com) and send a HTTP GET request over.

3. The server software will get this HTTP request. It will somehow generate a HTTP response and send that back trough the TCP connection. How the server does this is server software dependent.

4. When the browser gets the response, it typically renders it on screen. The HTTP request is now done.


## **Java HTTP Request example**

![HTTP Request](https://docs.oracle.com/javaee/6/tutorial/doc/figures/web-requestHandling.gif)


- **The HttpUrlConnection class** allows us to perform basic HTTP requests without the use of any additional libraries.

- Create a request, using **openConnection()** method of the URL class.
**setRequestMethod** method values are: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.
```
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```

- If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value to the OutputStream of the HttpUrlConnection instance.
```
Map<String, String> parameters = new HashMap<>();
parameters.put("param1", "val");

con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes(ParameterStringBuilder.getParamsString(parameters));
out.flush();
out.close();
```

- setRequestProperty() method, used to Add headers to a request:
`con.setRequestProperty("Content-Type", "application/json");`
the getHeaderField() method, used To read that value.
`String contentType = con.getHeaderField("Content-Type");`

- HttpUrlConnection class allows **setting the connect and read timeouts**, using these methods `setConnectTimeout(number) and setReadTimeout(number)`.


- Classes to handle cookies(that offered by java.net packages)-> **CookieManager and HttpCookie**.

- We can enable or disable automatically following redirects for a specific connection by using the **setInstanceFollowRedirects()** method with true or false parameter.

- Reading the response of the request can be done by parsing **the InputStream of the HttpUrlConnection instance**.

- If the request fails, trying to read the InputStream of the HttpUrlConnection instance won't work. Instead, **we can consume the stream provided by HttpUrlConnection.getErrorStream()**.

- It's not possible to get the full response representation using the HttpUrlConnection instance.
However, **we can build it using some of the methods that the HttpUrlConnection instance**
```
public class FullResponseBuilder {
    public static String getFullResponse(HttpURLConnection con) throws IOException {
        StringBuilder fullResponseBuilder = new StringBuilder();

        // read status and message

        // read headers

        // read response content

        return fullResponseBuilder.toString();
    }
}
```

[HOME](https://malkhaleel88.github.io/reading-notes)