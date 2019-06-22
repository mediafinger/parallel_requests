# Parallel Requests

---
Imagine you've got to make multiple requests.  
In parallel.  
In Ruby.

---
### Imagine you've got to make multiple requests.  
#### In parallel.  
##### In Ruby.  

---
## Possible workarounds

Every developer will find some way to handle this.

---
### Heavy dependencies

---
### Homemade asynchronicity

---
## Clean solution

---
### gem 'chimera_http_client', '~> 1.2.1.beta'

```ruby
queue.add(method, endpoint, success_handler: success_handler) # first
queue.add(method, other_endpoint) # second

responses = queue.execute

responses[0] # first
responses[1] # second
responses[2] # third, the call given in the success_handler
```

---
### chimera_http_client

Install it yourself:

    'chimera_http_client', '~> 1.2.1.beta'

https://github.com/mediafinger/chimera_http_client

---
## Thank you

<p>&nbsp;<p/>

Find this presentation

and several `code` examples

under: **https://github.com/mediafinger/parallel_requests**

<p>&nbsp;<p/>

### Andreas Finger &nbsp;&nbsp;&nbsp; @mediafinger
