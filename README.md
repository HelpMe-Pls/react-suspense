# What I've learnt
###### *For more details, see [`src/exercise/*.md`](https://github.com/HelpMe-Pls/react-suspense/tree/master/src/exercise) files*
-------------

## Simple Data-fetching
- Imagine when your app loads, you need some data **before** you can show anything useful. The best approaches to using `Suspense` involve kicking off the request for the data *as soon as* you have the information you need for the request. This is called the “**Render as you fetch**” approach.