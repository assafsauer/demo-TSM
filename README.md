# ACME Application with GNS  


```diff

BEFORE:
root@sauer-virtual-machine:/home/sauer/demo-TSM/cluter-1# curl -i --request HEAD -H 'Cache-Control: no-cache'  http://10.9.0.20/static/images/bottle_square.jpg
Warning: Setting custom HTTP method to HEAD with -X/--request may not work the 
Warning: way you want. Consider using -I/--head instead.
HTTP/1.1 200 OK
x-powered-by: Express
accept-ranges: bytes
content-length: 1955066
content-type: image/jpeg
last-modified: Wed, 06 Feb 2019 03:20:56 GMT
date: Tue, 21 Sep 2021 15:10:01 GMT
x-envoy-upstream-service-time: 21
server: istio-envoy

AFTER
root@sauer-virtual-machine:/home/sauer/demo-TSM/cluter-1# curl -i --request HEAD -H 'Cache-Control: no-cache'  http://10.9.0.20/static/images/bottle_square.jpg
Warning: Setting custom HTTP method to HEAD with -X/--request may not work the 
Warning: way you want. Consider using -I/--head instead.
HTTP/1.1 403 Forbidden
content-length: 19
content-type: text/plain
date: Tue, 21 Sep 2021 15:10:03 GMT
server: istio-envoy
x-envoy-upstream-service-time: 5

```
