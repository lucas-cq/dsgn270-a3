# DSGN270-A3 - Lucas Cummings

## User Story :
#### Skateboard Magazine
* As a skateboard magazine company I would like to show a skater of the day on my website, to display skaters for possible sponsorships and to maintain popularity in skateboarding.

* This integration would first save clients from asking me to update their page everytime they post. Skating is also a slowly dying industry, but if more people see the value in it (Like a new skateboard magazine) they will more likely sponsor new skaters. Skaters will also be incouraged to post their stunts, to hopefully get featured on the page. Bringing in more attention from the hashtags.

## Task Flow
1. Log into your business profile on instagram
2. Find a skater you would like to award skater of the day
3. Make a new post inlcuding the hashtag : #skateroftheday
4. Navigate back to your website
5. Refresh your website
6. Success! 

## Securing the API
To secure the API I used [this article](https://harrisonkolor.medium.com/using-the-instagram-api-serverless-netlify-to-display-your-own-photos-in-2021-7923014522d0) to add a Netlify toml file that points to a functions folder. In this folder is a script that uses axios and dotenv. Now all the tokens usually found in the ".env" file are secured in my Netlify environment variables. I wish Netlify had a feature where you could just add the actual .env file so the code still points to that file but only the user and Netlify have access to it.
This feature would remove a lot of hassle and dry up your code.

## API Info
* [API](https://developers.facebook.com/docs/instagram-basic-display-api)
* [Basic Setup](https://developers.facebook.com/docs/instagram-basic-display-api/getting-started)
* [Acess Tokens](https://developers.facebook.com/docs/instagram-basic-display-api/overview#instagram-user-access-tokens)
* [Display Media](https://developers.facebook.com/docs/instagram-basic-display-api/reference/media)

## Repo and Netlify
* [Repo](https://github.com/lucas-cq/dsgn270-a3)
* [Netlify](https://compassionate-carson-c8ddc9.netlify.app/)

### Attributions
* [Jan Kopriva](https://unsplash.com/photos/UMOrfrVby6M)
* [Tom Morbey](https://unsplash.com/photos/r1SwcagHVG0)
* [Tom Morbey](https://unsplash.com/photos/QJz32ZuCArg)
* [Remove a specific word in a string](https://www.codegrepper.com/code-examples/java/remove+specific+word+from+string+javascript)
* [Only display img with this key word](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes)
* [Using the Instagram API + Serverless Netlify to display your own Photos in 2021](https://harrisonkolor.medium.com/using-the-instagram-api-serverless-netlify-to-display-your-own-photos-in-2021-7923014522d0)
* Some style inspiration from [Thrasher](https://www.thrashermagazine.com/)