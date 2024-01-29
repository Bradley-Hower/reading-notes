# *Course 401 Python, Entry 16: Serverless Functions


**What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?**

- Pay for execution
- Develop in an language
- Faster dev cycle
- Cost-efficient
- Analytics
- Highly available

In comparison, server-based architecture requires one to run their own machines, at least one, and deal with all the administrative burdens associated with that. There is an advantage to this though, which is that latency issues can be eliminated, but the cost is significantly more.

Kubernetes: a container launching software used for setting up and managing containers.

Knative: a serverless framework for Kubernetes.

**How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?**

1. Build a project
2. Create a deployment
3. Set a domain name
4. Collaborate via comments

**What are APIs, and how can they be utilized in Python applications to access and manipulate data from external sources?**

An API (application programming interface) is an interface by which different software servers can communicate. While GraphQL is becoming more popular, REST is by far much more widely utilized. With Python, requests is the library which allows for interface with APIs.

To interact with APIs, various requests can be sent to either get, post, put (update), or delete.

**What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?**

The Requests library is the way to interact with APIs using Python.

Install via:

```
python -m pip install requests
```

Basic get request example:

```
import requests

r = requests.get('https://api.github.com/events')
```
To see what this data is, use ".text".

```
response.text
```

## Things I want to know more about

How different REST requests are in Python vs Javascript.
