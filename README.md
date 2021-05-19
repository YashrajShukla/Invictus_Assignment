INVICTUS PROJECT

Heroku link: https://yrs-invictus-assignment.herokuapp.com/

SCREENSHOTS - 

![Screenshot (53)](https://user-images.githubusercontent.com/60695111/118801787-05c51b00-b8bf-11eb-9778-77d02ecb6776.png)
![Screenshot (54)](https://user-images.githubusercontent.com/60695111/118801798-09f13880-b8bf-11eb-92f0-495c6ec8a727.png)
![Screenshot (55)](https://user-images.githubusercontent.com/60695111/118801809-0d84bf80-b8bf-11eb-86d4-e63366c776af.png)


# Installation:



```$ npm install```

```$ npm start```

# Resources used:


https://github.com/facebook/create-react-app/tree/master/packages/react-scripts/template#making-a-progressive-web-app


https://medium.com/byte-sized-react/hosting-react-and-a-rest-api-with-express-28f7ba5a4cc4



# Code Components:



```
wordArray = text.toLowerCase().split(/\W+/)
   wordArray.forEach((key) => {
        if (wordPool.hasOwnProperty(key)) {
            wordPool[key] += 1
        } else {
            wordPool[key] = 1
        }
    })
    wordCount = Object.keys(wordPool).map((key) => {
        return {
            word: key,
            count: wordPool[key]
            }
        })
        wordCount.sort((a,b) => b.count - a.count)
        return callback(wordCount)
```



In wordCounter function the text received from the url is stored in text and then split after each white space
and stored in wordArray. Count of words is determined by checking if wordPool.hasOwnProperty.
Then they are stored in wordCount which is an array of objects. This array is sorted and returns as many top results
as requested from the frontend.

```
    componentDidMount() {
        fetch('/data')
            .then(res => res.json())
            .then(data => this.setState({data: data}))
    }
```



Fetch from /data from the React component.






```
app.get('/data', (req, res) => {
    wordCounter('https://raw.githubusercontent.com/invictustech/test/main/README.md', (data) => {
        res.send(data)
    })
})
```
GET /data handled at the server end.



```
handleChange(event) {
        this.setState({number: event.target.value})
    }
```



Handling every time there is a change in the input box




        
        
        
        

# invictus_assignment

