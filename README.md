# mrequests
Using multiprocessing and requests to send requests using threads to fasten sending large number of requests.

## Usage
<pre>
from mrequests import MultiRequests
m = MultiRequests(method='GET')
urls = ["https://www.walmart.com/reviews/product/107","https://www.walmart.com/reviews/product/625"]
resp = m.send(urls)
for r in resp:
  print(r.status_code)
</pre>

## Future Work
<ul>
  <li>Parameterized requests</li>
  <li>Authenticated Sessions</li>
 </ul>
