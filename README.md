# React Go SSR Boilerplate

[![Go Report Card](https://goreportcard.com/badge/github.com/MrHuxu/react-go-ssr-boilerplate)](https://goreportcard.com/report/github.com/MrHuxu/react-go-ssr-boilerplate)

## Description

A boilerplate for fastly building web application based on React & Go using SSR(server side rendering).

![](https://raw.githubusercontent.com/MrHuxu/img-repo/master/react-go-ssr-boilerplate/react%20go%20boilerplate.gif)

## Requirements


1. Linux or Mac OS
2. Node.js (10.0.0 or higher)
3. Go (1.8.1 or higher)

## Features

- Frontend

  - [x] Components powered by [React](https://github.com/facebook/react)
  - [x] State management powered by [Redux](https://github.com/reactjs/redux)
  - [x] Stylesheet management powered by [styled-components](https://github.com/styled-components/styled-components)
  - [x] Fully-featured router management powered by [react-router](https://github.com/ReactTraining/react-router)
  - [x] Auto re-lint your js/jsx files after editing powered by [eslint-watch](https://github.com/rizowski/eslint-watch)

- Backend

  - [x] Manage the Go dependencies by [dep](https://github.com/golang/dep)
  - [x] Web framework powered by [Gin](https://github.com/gin-gonic/gin)
  - [x] Hot reload powered by another [Gin](https://github.com/codegangsta/gin)

## Usage

### For Development

1. Clone the repo and install all dependencies:


        go get github.com/MrHuxu/react-go-ssr-boilerplate && cd $GOPATH/src/github.com/MrHuxu/react-go-ssr-boilerplate

        go get -u github.com/golang/dep/cmd/dep
        dep ensure -v

        npm install

2. It's recommended to install the [React DevTools](https://github.com/facebook/react-devtools) and [Redux DevTools](https://github.com/gaearon/redux-devtools) for frontend debugging.

3. Launch the server:

        # execute the command below, then you'll see the dashboard shown
        # go visit http://localhost:8283 in your browser
        # editing any file will let the server or frontend reload

        go get -u github.com/codegangsta/gin
        npm run dev

### For Deployment

**It is highly recommended to use [Docker](https://www.docker.com/) to deploy this project!!**

#### Using Docker

1. Clone the repo and build Docker image:

        go get github.com/MrHuxu/react-go-ssr-boilerplate && cd $GOPATH/src/github.com/MrHuxu/react-go-ssr-boilerplate
        docker build . -t react-go-ssr-boilerplate
        docker run -p 13109:13109 -d react-go-ssr-boilerplate

2. Use `docker logs` command to monitor the logs of the server:

        docker logs -f [container_id]


#### Manually Build

1. Clone the repo and install all dependencies(same as above).

2. Launch the server:

        # go visit http://localhost:13109 in your browser after executing the command

        npm run prd
