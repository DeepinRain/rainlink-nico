# rainlink-nico
A plugin that allows you to play music on nicovideo.jp

Install
```
npm i rainlink-nico
```

Support source:
```
- https://www.nicovideo.jp/watch/sm30067009
```
How to
```js
const { Rainlink } = require('rainlink');
const { NicoPlugin } = require('rainlink-nico');

const rainlink = new Rainlink({
    library: new Library.DiscordJS(client),
    nodes: Nodes,
    plugins: [
      new NicoPlugin({
        searchLimit: 10,
      }),
    ],
});

rainlink.search(`https://www.nicovideo.jp/watch/sm30067009`); // track
rainlink.search('初音ミク', { engine: 'nicovideo' }); // search track using nico
```
