## log all env when starting application 

```
Map <String, String> map = System.getenv();
for (Map.Entry <String, String> entry: map.entrySet()) {
    log.info(" Environment Variable Name:- " + entry.getKey() + " Value:- " + entry.getValue());
}
```


## get header from http response 

```
Collection<String> headerCollection = httpResponse.getHeaderNames();
HashMap<String,String> headerMap = new HashMap<>();
for (String header : headerCollection) {
    headerMap.put(header,httpResponse.getHeader(header));
}
MDC.put("Headers", String.valueOf(headerMap));
```
