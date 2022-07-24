---
title: Introducing Multi-part Posts with Nested Routing
date: '2022-07-24'
tags: ['FastAPI', 'program']
draft: false
summary: 'FastAPI'
---

### Is concurrency is better than parallelism?

Nope! it is better on specific scenarios that involve a lot of waiting. It generally is a lot better than parallelism for web application development.

### `async` and `await`

Here is an example:
`burgers = await get_burgers(2)`
the key is the `await`. It tells Python that it has to wait for `get_burger(2)` to finish doing its thing before storing the results in `burgers`.
Python will know that it can go and do something else in the meanwhile.

For `await` to work, it has to be inside a function that supports this asynchronicity. You need to declare it with `async def:`

```python
@app.get('/burgers')`
    async def read_burgers() :
	burgers = await get_burgers(2)
    return burgers
```
