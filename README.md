# SkyLookup

Demo: https://siasky.net/NAC25yabWhK7AF0h0uJ-rrgAlIl0uyQnx8jQAhdJWVjqtw/

While [MiniSearch](https://github.com/lucaong/minisearch) and [AlaSQL](http://alasql.org/) are great in-browser full-text & SQL engines,
they can not handle GBs of data because of RAM limits.
SkyLookup is a bit different. It is a [Radix-tree](https://en.wikipedia.org/wiki/Radix_tree) (or radix trie) based file index.

# Performance

SkyLookup stores the data in alphabetical order in multiple files, and even if you has a tons of data, it will make only a few HTTP AJAX requests to find something:

- 1000 rows = 1 ajax request
- 1 million rows = 2 requests
- 1 billion rows = 3 requests
- 1000 billion rows = 4 requests

To add/update 1 row, you need to change the same amount of files that are required for lookup (1-4).
If you're building on [Sia Skynet](https://siasky.net), it is recommended to store the link of the latest index
file in a Skynet registry, so your users can access the updated database on the same link.

# Use-case examples

Presonally, I'll use SkyLookup to host [SkyLive](https://skylive.coolhd.hu) 100% to Skynet and to make a fully decentralized search engine, [DappDappGo](https://dappdappgo.coolhd.hu).
You can create a searchable dictionary or a decentralized Twitter where users can find other users profile pictures, etc.


![Tree index](https://www.researchgate.net/profile/Philippe_Fournier_Viger/publication/263696690/figure/fig1/AS:296556428316691@1447715970966/A-Prediction-Tree-PT-Inverted-Index-II-and-Lookup-Table-LT.png)
