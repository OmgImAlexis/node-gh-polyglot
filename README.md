
[![gh-polyglot](http://i.imgur.com/wQ2eGDb.png)](#)

# gh-polyglot

 [![Support me on Patreon][badge_patreon]][patreon] [![Buy me a book][badge_amazon]][amazon] [![PayPal][badge_paypal_donate]][paypal-donations] [![Version](https://img.shields.io/npm/v/gh-polyglot.svg)](https://www.npmjs.com/package/gh-polyglot) [![Downloads](https://img.shields.io/npm/dt/gh-polyglot.svg)](https://www.npmjs.com/package/gh-polyglot)

> Get language stats about GitHub users and repositories.

## :cloud: Installation

```sh
$ npm i --save gh-polyglot
```



Using this library on the client side is possible as well, but it's dependent on [`gh.js`](https://github.com/IonicaBizau/gh.js).

```html
<script src="path/to/gh.js"></script>
<script src="path/to/gh-polyglot.js"></script>
```

## :clipboard: Example



```js
// Dependencies
var GhPolyglot = require("gh-polyglot");

// Stats about git-stats
var me = new GhPolyglot("IonicaBizau/git-stats");

// Repository stats
me.repoStats(function (err, stats) {
    console.log(err || stats);
});

// User stats
me.userStats(function (err, stats) {
    console.log(err || stats);
});
```

## :question: Get Help

There are few ways to get help:

 1. Please [post questions on Stack Overflow](https://stackoverflow.com/questions/ask). You can open issues with questions, as long you add a link to your Stack Overflow question.
 2. For bug reports and feature requests, open issues. :bug:
 3. For direct and quick help from me, you can [use Codementor](https://www.codementor.io/johnnyb). :rocket:


## :memo: Documentation


### `GhPolyglot(input, token)`
Creates a new instance of `GhPolyglot`.

#### Params
- **String** `input`: The repository full name (e.g. `"IonicaBizau/gh-polyglot"`) or the username (e.g. `"IonicaBizau"`).
- **String** `token`: An optional GitHub token used for making authenticated requests.

#### Return
- **GhPolyglot** The `GhPolyglot` instance.

### `getAllRepos(callback)`
Gets all user's repositories.

#### Params
- **Function** `callback`: The callback function.

#### Return
- **Request** The request object.

### `repoStats(callback)`
Gets repository stats.

#### Params
- **Function** `callback`: The callback function.

#### Return
- **Request** The request object.

### `userStats(callback)`
Gets user stats.

#### Params
- **Function** `callback`: The callback function.

#### Return
- **Request** The request object.

### `check(callback)`
Wraps the callback in another function to manipulate the data.

#### Params
- **Function** `callback`: The callback function.

#### Return
- **Function** The wrapping function which gets the `err` and `data` arguments and changes the data converting it into an array.



## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :sparkling_heart: Support my projects

I open-source almost everything I can, and I try to reply everyone needing help using these projects. Obviously,
this takes time. You can integrate and use these projects in your applications *for free*! You can even change the source code and redistribute (even resell it).

However, if you get some profit from this or just want to encourage me to continue creating stuff, there are few ways you can do it:

 - Starring and sharing the projects you like :rocket:
 - [![PayPal][badge_paypal]][paypal-donations]—You can make one-time donations via PayPal. I'll probably buy a ~~coffee~~ tea. :tea:
 - [![Support me on Patreon][badge_patreon]][patreon]—Set up a recurring monthly donation and you will get interesting news about what I'm doing (things that I don't share with everyone).
 - **Bitcoin**—You can send me bitcoins at this address (or scanning the code below): `1P9BRsmazNQcuyTxEqveUsnf5CERdq35V6`

    ![](https://i.imgur.com/z6OQI95.png)

Thanks! :heart:


## :dizzy: Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:


 - [`github-stats`](https://github.com/IonicaBizau/github-stats)—Visualize stats about GitHub users and projects in your terminal.

## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[badge_patreon]: http://ionicabizau.github.io/badges/patreon.svg
[badge_amazon]: http://ionicabizau.github.io/badges/amazon.svg
[badge_paypal]: http://ionicabizau.github.io/badges/paypal.svg
[badge_paypal_donate]: http://ionicabizau.github.io/badges/paypal_donate.svg
[patreon]: https://www.patreon.com/ionicabizau
[amazon]: http://amzn.eu/hRo9sIZ
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(https%3A%2F%2Fionicabizau.net)&year=2015#license-mit
[website]: https://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
