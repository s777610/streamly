# streamly
This application was mainly built by React and Redux. I used redux-thunk as middleware to handle HTTP requests properly. In addition, it uses redux-form to simplify the workflow of development.

## Features
1. OAuth:<br>
Users can log in this application via google account. It implements OAuth 2.0. Add Google API into index.html, then we can call gapi library
` <script src="https//apis.google.com/js/api.js"></script>`

2. RTMP Server:<br>
I used [Node-Media-Server](https://github.com/illuspas/Node-Media-Server/) to serve my video streaming. It is easy to set up.

3. JSON Server:<br>
Stream video data is stored on [JSON Server](https://github.com/typicode/json-server/), which is a full fake PREST API. 

## Architecture
```
├── README.md
├── api
│   ├── db.json
│   ├── package-lock.json
│   └── package.json
├── client
│   ├── README.md
│   ├── package-lock.json
│   ├── package.json
│   ├── public
│   │   ├── favicon.ico
│   │   ├── index.html
│   │   └── manifest.json
│   └── src
│       ├── actions
│       │   ├── index.js
│       │   └── types.js
│       ├── api
│       │   └── streams.js
│       ├── components
│       │   ├── App.js
│       │   ├── GoogleAuth.js
│       │   ├── Header.js
│       │   ├── Modal.js
│       │   └── streams
│       │       ├── StreamCreate.js
│       │       ├── StreamDelete.js
│       │       ├── StreamEdit.js
│       │       ├── StreamForm.js
│       │       ├── StreamList.js
│       │       └── StreamShow.js
│       ├── history.js
│       ├── index.js
│       └── reducers
│           ├── authReducer.js
│           ├── index.js
│           └── streamReducer.js
└── rtmpserver
    ├── index.js
    ├── package-lock.json
    └── package.json
```