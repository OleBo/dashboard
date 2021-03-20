# covid-dashboard

![Language](https://img.shields.io/github/languages/top/Olebo/dashboard?style=for-the-badge)
![Code Quality](https://img.shields.io/lgtm/grade/python/github/Olebo/dashboard?style=for-the-badge)
![Repo Size](https://img.shields.io/github/repo-size/Olebo/dashboard?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/Olebo/dashboard?style=for-the-badge)
![Stars](https://img.shields.io/github/stars/Olebo/dashboard?style=for-the-badge)
![Forks](https://img.shields.io/github/forks/Olebo/dashboard?style=for-the-badge)
![Issues](https://img.shields.io/github/issues/Olebo/dashboard?style=for-the-badge)
![License](https://img.shields.io/github/license/Olebo/dashboard?style=for-the-badge)

A Coronavirus Dashboard that updates information realtime using [Streamlit](https://www.streamlit.io/) as the primary UI engine.

## Data Source

The [data source](https://github.com/CSSEGISandData/COVID-19) is the repository maintained by the Center of Systems Science and Engineering at
Johns Hopkins University. It is the same data source used to power the very famous [COVID dashboard](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6)

## Overview

Streamlit offers a beautiful UI to create data apps very easily. I was able to create the
side menu just using one line of code.

```python
import streamlit as st

st.sidebar.radio("Navigate", 
                 ["Home", "Data",
                  "Dashboard", "About", 
                  "Contribute"])
```

Similarly, one can create dropdowns, checkboxes and a bunch of other UI designs.
 ```python
import streamlit as st

st.sidebar.selectbox("Granularity", ["Worldwide", "Country"])

```

The graphs were created using plotly. Since streamlit supports multiple graphical libraries, rendering plotly 
chart were very easy. Just pass the plotly figure object into the `st.plotly_chart()` function.

```python
import streamlit as st
import plotly.express as px

fig = px.bar(x=df["X"], 
             y=df["Y"])

st.plotly_chart(fig)
```

## How to run

Clone the repository and install dependencies:

```shell script
pip3 install -r requirements.txt
```

Run the app using streamlit

```shell script
streamlit run app.py
```

## Contribute
Feel free to send pull requests and/or add issues.

## About

* [Github](https://github.com/OleBo)
