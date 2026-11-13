> **Archived (November 2026):** this project is no longer maintained. For concurrent HTTP requests, use [`concurrent.futures.ThreadPoolExecutor`](https://docs.python.org/3/library/concurrent.futures.html) with `requests`, or an async client such as [`httpx`](https://www.python-httpx.org/) or [`aiohttp`](https://docs.aiohttp.org/).

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
