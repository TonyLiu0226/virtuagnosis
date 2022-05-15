## Inspiration
Sometimes, seeing a doctor when you have symptoms is difficult. Oftentimes, doctor offices require you to book appointments days in advance, and are not open 24/7. Furthermore, walk in clinics and hospitals often have long wait times to see a doctor, just to find out what is causing your symptoms. So, what if you were able to just figure out the cause by going to a website, from the comfort of your own home? This is where virtuagnosis comes in.

## What it does
Users can select their symptoms via checkbuttons immediately upon loading into the website. Symptoms are convieniently grouped by body part, allowing users to easily find them. Once a user has selected all their symptoms, clicking a "predict disease" button will run a machine learning algorithm to generate a probable list of diseases they may have, which are displayed as cards below the button. The cards will contain basic information about the disease, as well as the full list of symptoms associated with it. There will always be 5 probable diseases generated each time the predict disease button is clicked, in case some of the predictions turn out to be inaccurate (our ml wasn't perfect).

## How we built it
We used the Svelte.js framework for the front end, along with CSS styling for the webpages. Our backend uses a flask server to get disease and symptom data, and to call our machine learning algorithm when a user presses the predict disease button. The machine learning algorithm compares the symptoms of each disease with the user entered symptoms, and uses the euclidean distance logic of K nearest neighbors, plus a scoring algorithm to determine the five diseases that the user most likely might have.

## Challenges we ran into
Our machine learning algorithm needed a lot of tweaking to generate optimal results. We also had to diverge from the basic KNN algorithm in order to do so. Another big challenge was surprisingly the front end. We were relatively new to Svelte (and JavaScript in general), so we had trouble figuring out things that turned out to be slightly trivial in the end. However, this is naturally part of the learning experience. Also, we couldn't CSS properly apparently :((

## Accomplishments that we're proud of and what we learned
- We made the app in 12 hours. We initially had a different idea that we started on during the first day of the hackathon, but then decided to ditch that for this idea due to this one being much more practical
- We learned how to make animated objects in web apps. Our app has smooth animations and transitions, something that we completely skipped out on in our earlier projects
- We learned a lot about front end web development, and the basics of machine learning

## Improvements
- The ability to keep track of users' previous symptoms. This can be used to help improve the machine learning for that particular user, to predict diseases more accurately based on their prior reported symptoms. We will need to implement user authentication for this.
- Improve the front end UI to maybe include a human body anatomy that is interactive. Clicking on certain parts of the body will list symptoms specific to that part, which will make it even easier for users to find their symptoms
- Add info on possible remedies for diseases on the disease cards
