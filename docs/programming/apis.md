# APIs

## API Basics
> Application Programmable Interface

Explain?
its the messenger that takes requests and tells a system what you want to do, and returns the response back to you
Allows different apps and services to exchange information
they assist us in completing tasks we need to perform by abstracting away complexity
The tools used to connect the front end to the backend
Connects apps together
its where you have the permission to use someone elses code in your application
Access Data from 3rd parties
Hide complexity and perform tasks
Extend functionality
Security HTTP accessing a website..
hypertext transfer protocol
URI GET (it receives data) from server using url path
Response (HTML) browser can now render page a form
URI POST (submitting/posting data to the server)
Examples
'yeet!'.toUpperCase() // <- API
"Login with Google"
Weather app using WeatherChannel API
REST, GraphQL
Twilio for text messaging
Stripe for payments
Types of API SOAP, REST, GRAPHQL, RPC Remote API
Google Translate, Shazam
the processing is happening elsewhere REST
Representational State Transfer
GraphQL
RESTful API
API Defintion
shape of data needed
API Key
unique identifier key
API Gateway
REST API
Representational State Transfer

RESTful API
GraphQL
Program sends GET request to a URI
server responds with data (JSON ) and HTTP Headers
JSON - Javascript Object Notation
CRUD

GET (Read), POST (Create),( PUT, PATCH (Update)), DELETE (Deleting)
Client-Server Architecture

client = your program
protocol used = http
Statelessness

stateless = server wont remember anything about your client
login
Resources and Collections

used to reference an object, or collections of objects
imagine a book store, each book is a resource
click it, the link to the author is also a resource
with a photo sharing app, each user is a resource
each photo is a resource
alums are resources
Layered System

spotify is a layered system
not rendered on every request
Cacheability

Uniform Design

Code on Demand

const myArray = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

myArray.map((myNum) => {
  console.log('Hello ', myNum)
})
use a filter before a map to filter out all the undefined values

myArray.filter((myNum) => {
  return myNum > 5
})
check for undefined (type checking )
>  a => !!a.fav
<  a => !!a.fav
>  const moo = {a: 1}
<  undefined
>  !!moo.a
<  true
>  const mooo = {a: null}
<  undefined
async await
the fetch api is promise based

it excecutes something, resolves it
and that gives us access to a .then
const listRepos = async (username) => {
  const repos = await fetch(
    `https://api.github.com/users/${username}/repos?type=owner&sort=updated`
  )
    .then((res) => res.json())
    .catch((error) => console.error(error))
}
Fetch my Github Repos
getting all the Github repos, the code url, the description, the website url, the topics

Github API reference I looked here to find the correct keys I wanted

const listRepos = async (username) => {
  const repos = await fetch(
    `https://api.github.com/users/${username}/repos?type=owner&sort=updated`
  )
    .then((res) => res.json())
    .catch((error) => console.error(error))

  const markup = repos
    .map(
      (repo) => `
             <li>
                <h2>${repo.name}</h2>
                <p>${repo.description}</p>
                <label>${repo.topics}</label>
                <div/>

                <a href="${repo.homepage}">demo</a>
                <a href="${repo.html_url}">code</a>
            </li>

            `
    )
    .join('')

  const content = document.getElementById('content')
  content.innerHTML = `<ul>${markup}</ul>`
}

listRepos('newtcandoit')
next I want to capture screenshots of each deployed website to display with this information too

SDKs
Software Development Kit

what?
a toolbox of code that calls apis for you
Analyse repsonse model object
Topics

Tutorials
How to use APIs

Serverless Cloud: Next-Gen Serverless App Platform

Resources

public-apis/public-apis

What is an API Gateway?

A collective list of APIs. Build.

What is a REST API?

API basics for you (2020) | What is API | Explained with simple examples

rest-apis

What is an Application Programming Interface (API)

Next.js + Spotify API beginner tutorial - learn Jamstack [Twitch Stream Highlights]

Completed tutorials API vs. SDK: What's the difference?What is an API and how does it work? (In plain English)