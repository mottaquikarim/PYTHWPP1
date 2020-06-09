# Simple Finance Service

Let's build a simple Finance service. This service will primarily deal with providing us with useful information about the stock market.

## Step 1: download and test [yfinance](https://github.com/ranaroussi/yfinance)

First, we need to install the `yfinance` module.

### Unix
```
pip3 install yfinance --user
```

### PC
```
pip install yfinance --user
```

Let's test this:

```
msft = yf.Ticker("MSFT")
msft.history(period="1d").to_json()
```

More periods [here](https://github.com/ranaroussi/yfinance/blob/9e05bfa9500899fc1b7307f79bf3c76b82a94727/yfinance/multi.py#L40)

## Step 2: setting up a simple flask server

Build a server that will return _only_ the result above, but via API call.

Endpoint: `http://127.0.0.1:5000/`

## Step 3: parameterized responses

Build a server endpoint that will return specifically the stocks for comapny in question:

Endpoint: `http://127.0.0.1:5000/company/MSFT` -- gives us microsoft stock for 5d
Endpoint: `http://127.0.0.1:5000/company/ORCL` -- gives us oracle stock for 5d

## Step 4: parameterized responses with also a period (must be valid period)

Endpoint: `http://127.0.0.1:5000/company/MSFT/period/5d` -- gives us microsoft stock for 5d
Endpoint: `http://127.0.0.1:5000/company/MSFT/period/1h` -- gives us microsoft stock for 1h

## Step 5: html output!

Now let's build a way to spit out HTML

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
  return render_template('index.html', name="hi!")
  # what would happen if you set name to: request.args.get('user', "test")?
```
To do this, we need an `templates` folder!

## Step 6: Same as step 4 but with HTML

Did you know that if you ran `to_html()` it returns HTML?!

Implement the following:

Endpoint: `http://127.0.0.1:5000/company/MSFT/period/5d/index.html` -- gives us microsoft stock for 5d
Endpoint: `http://127.0.0.1:5000/company/MSFT/period/1h/index.html` -- gives us microsoft stock for 1h

This will give us HTML output!

<table border="1" class="dataframe"><thead><tr style="text-align: right;"><th></th><th>Open</th><th>High</th><th>Low</th><th>Close</th><th>Volume</th><th>Dividends</th><th>Stock Splits</th></tr><tr><th>Date</th><th></th><th></th><th></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><th>2020-06-03</th><td>184.82</td><td>185.94</td><td>183.58</td><td>185.36</td><td>27311000</td><td>0</td><td>0</td></tr><tr><th>2020-06-04</th><td>184.30</td><td>185.84</td><td>182.30</td><td>182.92</td><td>28761800</td><td>0</td><td>0</td></tr><tr><th>2020-06-05</th><td>182.62</td><td>187.73</td><td>182.01</td><td>187.20</td><td>39893600</td><td>0</td><td>0</td></tr><tr><th>2020-06-08</th><td>185.94</td><td>188.55</td><td>184.44</td><td>188.36</td><td>33171000</td><td>0</td><td>0</td></tr><tr><th>2020-06-09</th><td>188.00</td><td>190.70</td><td>187.26</td><td>189.80</td><td>28820688</td><td>0</td><td>0</td></tr></tbody></table>

## Step 7: HTML base

Might not get here...
```html
<!doctype html>
<html>
<head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    <link rel="stylesheet" href="{{ url_for('static', filename='styles/main.css') }}"/>
    <title>{% block title %}{% endblock %}</title>
</head>
<body>
    {% block content %}
    {% endblock %}
</body>
</html>
```

in templates

```
{% extends "base.html" %}
{% block title %}User Page{% endblock %}
{% block content %}
<h1>Hello, {{name}}!!</h1>
{% endblock %}
```

## Step 8: bootstrap and static files!

```
<link rel="stylesheet" href="{{ url_for('static', filename='styles/main.css') }}"/>
```
