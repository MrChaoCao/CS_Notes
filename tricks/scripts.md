"scripts": {
   "server": "rails s",
   "frontend": "webpack --watch",
   "dev": "concurrently \"npm run server\" \"npm run frontend\"",
   "postinstall": "webpack"
 },

if you install concurrently (npm install --save concurrently), then add those scripts, you cn run npm run dev to run your webpack and rails server in the same terminal window.
