# Dumb Bot API `v1.0.2`
A package to interact Dumb Bot List API.


<a href="https://www.npmjs.com/package/dumb-botlistjs/"><img src="https://img.shields.io/npm/v/dumb-botlistjs.svg?maxAge=3600" alt="NPM version" /></a>
<a href="https://www.npmjs.com/package/dumb-botlistjs"><img src="https://img.shields.io/npm/dt/dumb-botlistjs.svg?maxAge=3600" alt="NPM downloads" /></a>


<a href="https://nodei.co/npm/dumb-botlistjs"><img src="https://nodei.co/npm/dumb-botlistjs.png?downloads=true&stars=true" alt="npm installnfo" /></a>

#### Instalation
To install this package please run `npm install dumb-botlistjs`

#### Example of usage
```js
const botlist = require("dumb-botlistjs");
const dbl = new botlist("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  // console.log("Server count posted")
  let hasVote = await dbl.hasVoted("714451348212678658");
  if(hasVote === true) {
    console.log("Voted");
  } else {
    console.log("Vote please.");
  }
  
  
  let search = await dbl.search("779641401482805289");
  console.log(search);
  /*
  { RESULTS :
    avatar: 'https/cdn.discordapp.com/avatars/807855659173150781/f360c03f3ba6705c4d994b4edb19a634.webp?width=100&height=100',
    botID: '828959241586606110',
    username: 'Dhvit',
    discrim: '4006',
    shortDesc: 'An op bot',
    prefix: '.,
    votes: 20,
    ownerID: '720632216236851260',
    owner: 'DhvitisOP',
    coowners: [ '' ],
    tags: [ 'Moderation', 'Reddit', 'Music' ],
    longDesc: "An Another OP bot",
    certificate: 'not Certified'
  }
  */
});```
