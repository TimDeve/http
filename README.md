# http

HTTP for Carp, expressed as a parser and a data structure.

## Installation

```clojure
(load "git@github.com:carpentry-org/http@0.0.3")
```

## Usage

Currently, all you can do is parse and build HTTP requests and responses, by
using `Request.parse` and `Response.parse`.

Hopefully you’ll soon be able to do more than that!

```clojure
(load "git@github.com:carpentry-org/http@0.0.3")

(def txt "POST / HTTP/1.1
Host: https://veitheller.de
User-Agent: curl/7.54.0
Accept: */*

hi!")

(defn main []
  (let [x (Request.parse txt)]
    (match x
      (Result.Success r) (println* &r)
      (Result.Error e)   (println* &e))))
```

<hr/>

Have fun!
