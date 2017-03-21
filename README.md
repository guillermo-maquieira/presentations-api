# Presentations List API Client

Application that consists on an API REST using Flask (Python) and Knockout.js

## Heroku

An app deploy has been done [here](https://presentations-api.herokuapp.com/index.html)

## Screenshot

![]
(https://raw.githubusercontent.com/guillermo-maquieira/presentations-api/master/demo.png)

## Request & Response Examples

### GET /presentations

Get all presentations.

Example: https://presentations-api.herokuapp.com/api/presentations

Response body:

```json
{
	"presentations": [
		{
			"createdAt": "March 6, 2014",
			"creator": {
				"name": "consectetur laborum",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f432fbb67217182785",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt amet ad nostrud"
		},
		{
			"createdAt": "July 31, 2015",
			"creator": {
				"name": "cupidatat excepteur",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f4d62116d1231786ca",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "Lorem commodo excepteur minim"
		}
	]
}
```

### GET /presentations/{id}

Get a single presentation by id.

Example: https://presentations-api.herokuapp.com/api/presentations/56f137f432fbb67217182785

Response body:

```json
{
	"presentation": [
		{
			"createdAt": "March 6, 2014",
			"creator": {
				"name": "consectetur laborum",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f432fbb67217182785",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt amet ad nostrud"
		}
	]
}
```

### GET /presentations/search/{term}

Get all presentations matching a certain term.

Example: https://presentations-api.herokuapp.com/api/presentations/search/incididunt

Response body:

```json
{
	"presentations": [
		{
			"createdAt": "March 6, 2014",
			"creator": {
				"name": "consectetur laborum",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f432fbb67217182785",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt amet ad nostrud"
		},
		{
			"createdAt": "February 25, 2016",
			"creator": {
				"name": "velit occaecat",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f4b3f1ed19ede3ca50",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt eiusmod nostrud duis"
		},
		{
			"createdAt": "March 15, 2016",
			"creator": {
				"name": "excepteur eu",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f4f5b6403e6fef99d5",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt sint eiusmod labore"
		},
		{
			"createdAt": "January 23, 2016",
			"creator": {
				"name": "laborum irure",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f5cf4aa21b3f32a193",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "ipsum incididunt est quis"
		},
		{
			"createdAt": "February 8, 2016",
			"creator": {
				"name": "labore ut",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f5dd7b9754d59938b6",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "duis elit magna incididunt"
		},
		{
			"createdAt": "November 13, 2014",
			"creator": {
				"name": "eiusmod tempor",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f5eb6489b17e9eaa04",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt in anim Lorem"
		}
	]
}
```

### GET /presentations/sortasc

Get all presentations sorted by ascending date.

Example: https://presentations-api.herokuapp.com/api/presentations/sortasc

```json
{
	"presentations": [
		{
			"createdAt": "March 15, 2016",
			"creator": {
				"name": "excepteur eu",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f4f5b6403e6fef99d5",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt sint eiusmod labore"
		},
		{
			"createdAt": "March 3, 2016",
			"creator": {
				"name": "sit labore",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f47f173c645a6f6dcf",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "reprehenderit enim cillum est"
		},
		{
			"createdAt": "February 25, 2016",
			"creator": {
				"name": "velit occaecat",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f4b3f1ed19ede3ca50",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt eiusmod nostrud duis"
		},
		{
			"createdAt": "February 8, 2016",
			"creator": {
				"name": "labore ut",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f5dd7b9754d59938b6",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "duis elit magna incididunt"
		}
	]
}
```

### GET /presentations/sortdesc

Get all presentations sorted by descending date.

Example: https://presentations-api.herokuapp.com/api/presentations/sortdesc

```json
{
	"presentations": [
		{
			"createdAt": "March 15, 2016",
			"creator": {
				"name": "excepteur eu",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f4f5b6403e6fef99d5",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt sint eiusmod labore"
		},
		{
			"createdAt": "March 3, 2016",
			"creator": {
				"name": "sit labore",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f47f173c645a6f6dcf",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "reprehenderit enim cillum est"
		},
		{
			"createdAt": "February 25, 2016",
			"creator": {
				"name": "velit occaecat",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f4b3f1ed19ede3ca50",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "incididunt eiusmod nostrud duis"
		},
		{
			"createdAt": "February 8, 2016",
			"creator": {
				"name": "labore ut",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f5dd7b9754d59938b6",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "duis elit magna incididunt"
		},
		{
			"createdAt": "February 2, 2016",
			"creator": {
				"name": "laborum do",
				"profileUrl": "http://randomprofile.prezi.com/"
			},
			"id": "56f137f5bb6d1daae54272b9",
			"thumbnail": "https://placeimg.com/400/400/any",
			"title": "mollit reprehenderit nulla magna"
		}
	]
}
```
