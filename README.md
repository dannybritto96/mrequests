# mrequests
Using multiprocessing and requests to send requests using threads to fasten sending large number of requests.

## Usage
```python
from mrequests import PoolRequests
m = PoolRequests(method="GET")
m.headers_update({"Cache-Control": "no-cache"})
m.set_basic_auth("username","password")
urls = ["https://www.google.com","https://www.yahoo.com"]
resp = m.send(urls)
for r in resp:
  print(r.status_code)
```

## Installation
<pre>
pip install mrequests
</pre>


## Future Work
<ul>
  <li>Parameterized requests</li>
 </ul>
