# JJE Web Design

## Overview
This markdown serves as an outline of the technical matters and priorities of JJE Web Design, including both this template and the general workflows and responsibilities, since this will get cloned out for each client.

The format of the app itself is a simple To Do List, as this has full CRUD functionality without having to work too hard.

## Tech Stack
### Frontend
- Svelte for frontend design, using components instead of classes to keep things simple
- CSS is [Skeleton](http://getskeleton.com), so as to have some style while keeping it minimalistic

### Backend
- We are using [Sanity.io](https://www.sanity.io), as this is how clients will be interfacing with their apps
- This implementation uses dotenv modules to keep Contentful API keys secure. This is done through src/utils/dotenv.js, then imported into the app


## Steps in the Process
- The repo should be cloned once basic client needs are understood and UI/UX has informed the Frontend Engineer what functions are needed
- Frontend functionality should be gotten together
- Design should come around this point, which should then be replicated as closely as possible (*Note, keep an eye out for mobile responsiveness in design to save double work*)
- Once done, should coordinate with UI/UX for testing and make a Contentful model to test backend integration


## Conclusion
Happy coding!