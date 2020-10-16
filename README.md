# SkyLookup

Demo: https://siasky.net/NAC25yabWhK7AF0h0uJ-rrgAlIl0uyQnx8jQAhdJWVjqtw/

While [MiniSearch](https://github.com/lucaong/minisearch) is a great in-browser search engine for full-text,
it can not handle more than some MBs of data.
SkyLookup is a bit different. It is a directory-tree based indexed key-value database.
You can only store string pairs, but it can handle any amount of rows and it does only 2-4 HTTP requests.

SkyLookup stores the data in alphabetical order in multiple files, and even if you have a 1000 files (1 million rows), it will make only 2 ajax requests to find the result.

Try it out: soon

![Tree index](https://www.researchgate.net/profile/Philippe_Fournier_Viger/publication/263696690/figure/fig1/AS:296556428316691@1447715970966/A-Prediction-Tree-PT-Inverted-Index-II-and-Lookup-Table-LT.png)
