# flutter_emoji

👉 A light-weight Emoji 📦 for Flutter with all up-to-date emojis 😄. Made from 💯% ☕ with ❤️!

Inspired from the [node-emoji](https://github.com/omnidan/node-emoji) package.

## Installation

Add this into `pubspec.yaml`

```
dependencies:
  flutter_emoji: ">= 2.0.0"
```

## API Usage

First, import the package:

```
import 'package:flutter_emoji/flutter_emoji.dart';
```

There are two main classes you need to know to handle Emoji text: `Emoji` and `EmojiParser`.

Basically, you need to initialize an instance of `EmojiParser`.

```
var parser = EmojiParser();
var coffee = Emoji('coffee', '☕');
var heart  = Emoji('heart', '❤️');

// Get emoji info
var emojiHeart = parser.info('heart');
print(emojiHeart); '{name: heart, full: :heart:, code: ❤️}'

// Check emoji equality
heart == emojiHeart;  // returns: true
heart == emojiCoffee; // returns: false

// Get emoji by name or code
emoji.get('coffee');   // returns: Emoji{name="coffee", full=":coffee:", code="☕"}
emoji.get(':coffee:'); // returns: Emoji{name="coffee", full=":coffee:", code="☕"}

emoji.hasName('coffee'); // returns: true
emoji.getName('coffee'); // returns: Emoji{name="coffee", full=":coffee:", code="☕"}

emoji.hasEmoji('❤️'); // returns: true
emoji.getEmoji('❤️'); // returns: Emoji{name="heart", full=":heart:", code="❤️"}

emoji.emojify('I :heart: :coffee:'); // returns: 'I ❤️ ☕'
emoji.unemojify('I ❤️ ☕'); // returns: 'I :heart: :coffee:'
```

## TODO

Features coming to this package:

- [x] Get detail of an emoji.
- [x] Refactor for easier usage.
- [ ] Validate bad input.
- [ ] Find list of available emojis from a given text.
- [ ] Replace emoji by another one.
- [ ] Callback for handling missing emojis on general methods.
- [ ] Auto-update emoji list.
- [ ] Make extensible emoji matcher.

## License

[MIT](LICENSE.md) @ 2019 [Pete Houston](https://petehouston.com).
