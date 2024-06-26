## create project from cli 

```bash
curl https://start.spring.io/starter.zip \
    -d type=maven-project \
    -d bootVersion=3.2.1 \
    -d dependencies=web \
    -d javaVersion=17 \
    -d name=helloworld \
    -d artifactId=helloworld \
    -d baseDir=helloworld \
    -o helloworld.zip
unzip helloworld.zip
cd helloworld

```


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
