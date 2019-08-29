# Initial Setup

Create a new [GitHub](https://github.com/) repository and name it `data-structures`  
All of your work for this class should be kept in this (well-organized!) repository.

# Weekly Assignment 1

### Due Friday 8/30 at 6:00pm

## Part One

1. Using Node.js (in Cloud 9), make a request for each of the ten "Meeting List Agenda" pages for Manhattan. **Important: show the code for all ten requests.**    


> Note: you will creating your own Cloud 9 environment from your personal AWS account for your work in this course. Do not use the Major Studio AWS account that Daniel sent you. You will incur some expenses on AWS but they are very unlikely to exceed what you get on the free tier plus the $100 credit you receive from signing up for AWS Educate. 

2. Using Node.js: For each of the ten files you requested, save the body as a **text file** to your "local" environment (in AWS Cloud9).

3. Study the HTML structure and tags and begin to think about how you might parse these files to extract relevant data for these AA meetings.

4. Update your GitHub repository with the relevant files: your `js` file and ten `txt` files, plus a `md` file with your documentation. In Canvas, submit the URL of the specific location of this work within your `data-structures` GitHub repository. 

## Starter code

```javascript
// npm install request
// mkdir data

var request = require('request');
var fs = require('fs');

request('https://parsons.nyc/thesis-2019/', function(error, response, body){
    if (!error && response.statusCode == 200) {
        fs.writeFileSync('/home/ec2-user/environment/data/thesis.txt', body);
    }
    else {console.log("Request failed!")}
});
```
### Thoughts
