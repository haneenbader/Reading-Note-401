#  WRRC and Java

***Step 1: Local Processing***

HTTP request lifecycle is being made by a browser, as opposed to cURL, an API client like Postman, or some other app.

Your browser extracts the "scheme"/protocol (we have established
that this will be HTTP), host (www.example.com), and optional port number, resource path, and query strings. `<protocol>://<host><:optional port>/<path/to/resource><?query>` , `|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|`.

***Step 2: Resolve an IP***

- The DNS request contains the preconfigured IP for your DNS server and your return IP in its header. 

- Once your request arrives at your configured DNS server, the server looks for the address associated with the requested hostname.

***Step 3: Establish a TCP Connection***

- One of the key differences between TCP and UDP is that TCP ensures delivery and ordered data transmission.

- TCP connections are opened using what’s known as a three-way handshake.  


* Creating a Request

We can create an HttpUrlConnection instance using the openConnection() method of the URL class. The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

`URL url = new URL("http://example.com");` 
`HttpURLConnection con = (HttpURLConnection) url.openConnection();`
`con.setRequestMethod("GET");`

* Adding Request Parameters

< 
   public class ParameterStringBuilder {

    public static String getParamsString(Map<String, String> params) 

      throws UnsupportedEncodingException{

        StringBuilder result = new StringBuilder();

        for (Map.Entry<String, String> entry : params.entrySet()) {
          result.append(URLEncoder.encode(entry.getKey(), "UTF-8"));
          result.append("=");
          result.append(URLEncoder.encode(entry.getValue(), "UTF-8"));
          result.append("&");
        }

        String resultString = result.toString();
        return resultString.length() > 0
          ? resultString.substring(0, resultString.length() - 1)
          : resultString;
    }}
>

* Setting Request Headers

`con.setRequestProperty("Content-Type", "application/json");`

* Configuring Timeouts

These values define the interval of time to wait for the connection to the server to be established or data to be available for reading.

`con.setConnectTimeout(5000);`
`con.setReadTimeout(5000);`
