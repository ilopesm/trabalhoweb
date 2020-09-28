const { request, response } = require('express')
const express = require('express')
const twit = require('twit')
const app = express()

var T = new twit({
    consumer_key:         'MUjajDDwrVJSCAdefbgsZbcqI',
    consumer_secret:      'Fc3ILFaxrzKgMQJchlJzsSUOY0L9Q1sYjY7o6CSCAylRLAwhw9',
    access_token:         '276747917-AAtb98Wmew4dXPxblCxMGQ4lVn6Qd3zUA5sS9r9i',
    access_token_secret:  'jNHIc1wO1cupj7S6l2Fiu55ayccZjIe8N78Oze6GIQN20',
    timeout_ms:           60*1000,  
    strictSSL:            true,     
})
app.get('/toptrends',(request,response)=>{

    T.get('https://api.twitter.com/1.1/trends/place.json?id=455827',(err,data,response)=>{

        for(let eachData of data){
            console.log(eachData)
        }

    })
    response.sendStatus(200);
})

app.get('/tweetts',(request,response)=>{

    T.get('https://api.twitter.com/1.1/statuses/user_timeline.json?screen_name=furia&count=2',(err,data,response)=>{

        for(let eachData of data){
            console.log(eachData)
        }

    })
    response.sendStatus(200);
})


app.listen(9898)