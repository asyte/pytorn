# pytornapi
A python based wrapper for the Torn API. This can be used in your code to easily interact with Torn API endpoints fromy our python code.

## Quickstart
### Using PyTorn in your code
```
from pytornapi import PyTornAPI
...
```

### API Keys
You must use at least a public api key to access any torn api endpoints.  Please be aware of the rate limitations as described in the [Torn API Documentation](https://www.torn.com/api.html#).

You can set a default api key to be used any time an API call is made.
```
# Set a default api key
PyTornAPI.set_key(MY_API_KEY)
```

You can also pass an API key with each request as such:
```
user_data = PyTornAPI.get("user", "basic", user_id=2203763, key=MY_API_KEY)
```

### Async
PyTornAPI fully facilitates asynchronous use through the `aget_` methods
```
user_data = await PyTornAPI.aget("user", "basic", user_id=2203763)
```

### URL For Endpoints
Sometimes you just need to know te url endpoint
```
user_data_url = PyTornapi.url_for("user", "basic", user_id=2203763)
```
