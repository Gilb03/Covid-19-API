# coronavirus-Heroku-tracker (API)

> This is a fast (< 200ms) and basic API for tracking development of the new coronavirus (2019-nCoV). It's written in Python using 🍼 Flask.

[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
![GitHub last commit](https://img.shields.io/github/last-commit/Omaroid/Covid-19-API)
![GitHub pull requests](https://img.shields.io/github/issues-pr/Omaroid/Covid-19-API)
![GitHub issues](https://img.shields.io/github/issues/Omaroid/Covid-19-API)

## Endpoints

All requests must be made to the base url: ``https://covid19api.herokuapp.com/``. You can try it out in your browser to further inspect responses.

Getting confirmed cases, deaths, and recoveries:

```http
GET /
```
```json
{ "latest": { ... }, "confirmed": { ... }, "deaths": { ... }, "recovered": { ... } }
```

## Data

The data comes from the [2019 Novel Coronavirus (nCoV) Data Repository, provided
by JHU CCSE](https://github.com/CSSEGISandData/2019-nCoV). It is
programmatically retrieved, re-formatted and stored in the server for one hour.

I've also programmed a skeduler on Heroku to run the refresh script every day since the data there is updated daily.

## Prerequisites

You will need the following things properly installed on your computer.

* [Python 3](https://www.python.org/downloads/) (with pip)
* [Flask](https://pypi.org/project/Flask/)

## Installation

* `git clone https://github.com/Omaroid/Covid-19-API.git`
* `cd Covid-19-Api`
* `pip install requirements.txt`

## Running / Development

* `python app.py`
* Visit your app at [http://localhost:5000](http://localhost:5000).

### Building

### Deploying

* Create a Heroku account
* Create a Heroku application
* `heroku login`
* `git init`
* `heroku git:remote -a <AppName>`
* `git add .`
* `git commit -am "first commit"`
* `git push heroku master`

### Deploying

* Visit your application webpage
* `https://<AppName>.herokuapp.com/`

## License

The data is available to the public strictly for educational and academic research purposes.