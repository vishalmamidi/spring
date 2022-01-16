## get header from http response 
```
Collection<String> headerCollection = httpResponse.getHeaderNames();
HashMap<String,String> headerMap = new HashMap<>();
for (String header : headerCollection) {
    headerMap.put(header,httpResponse.getHeader(header));
}
MDC.put("Headers", String.valueOf(headerMap));
```
