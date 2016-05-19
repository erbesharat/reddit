# reddit

A simple go package that gets latest topics of a subreddit 

# How to use
First you should get the package with go tool
```
go get github.com/erbesharat/reddit
```
After that you can import the package in your code
```
package main

import (
	"fmt"
	"log"
	"github.com/erbesharat/reddit"
)

func main() {
	topics, err := reddit.Get("SubredditName")
	if err != nil {
		log.Fatal(err)
	}
	for _, topic := range topics {
		fmt.Println(topic)
	}
}
```
