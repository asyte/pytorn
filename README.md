# pytornapi
A python based wrapper for the Torn API. This can be used in your code to easily interact with Torn API endpoints fromy our python code.

## Quickstart
### Using PyTorn in your code
```
from pytornapi import PyTornAPI
...

user_data = PyTornAPI.get("user", "basic", user_id=2203763, key=MY_API_KEY)

```

### API Keys
You must provide, at the the very least, a public torn api key to access any torn api endpoints. As you've seen, you can pass a key with each api request using the `key` argument. You can also set a default api key to be used any time an API call is made.
```
# Set a default api key
PyTornAPI.set_key(MY_API_KEY)
user_data = PyTornAPI.get("user", "basic", user_id=2203763)
```
> **_NOTE:_** Please be aware of the rate limitations as described in [the Torn API Documentation](https://www.torn.com/api.html#) as well as which endpoints are supported by which key types.

### Async
PyTornAPI fully facilitates asynchronous use through the `aget_` methods
```
user_data = await PyTornAPI.aget("user", "basic", user_id=2203763)
```

### URL For Endpoints
Sometimes you just need to know te url endpoint
```
user_data_url = PyTornAPI.url_for("user", "basic", user_id=2203763)
```

### Exceptions
Various exceptions can be raised in the context of getting data from the torn api. PyTornAPI does its best to obfuscate these exceptions.
```
try:
    user_data_url = PyTornAPI.get("user", "basic", user_id=2203763)
```
