# What I've learnt
###### *For more details, see [`src/exercise/*.md`](https://github.com/HelpMe-Pls/react-suspense/tree/master/src/exercise) files*
-------------

## Simple Data-fetching
- Use `Suspense` in conjunction with `ErrorBoundary` ([at 2:00](https://epicreact.dev/modules/react-suspense/simple-data-fetching-extra-credit-solution-1)) to handle runtime errors as well as errors while fetching data. 
- SoC by abstracting data fetching handlers [into a module](https://epicreact.dev/modules/react-suspense/simple-data-fetching-extra-credit-solution-3).  


## Render as you fetch
- Imagine when your app loads, you need some data **before** you can show anything useful. The best approaches to using [`Suspense`](https://reactjs.org/docs/react-api.html#reactsuspense) involve kicking off the request for the data *as soon as* you have the information you need for the request. This is called the “**Render as you fetch**” approach ([at ]()).
- [The positioning](https://epicreact.dev/modules/react-suspense/render-as-you-fetch-extra-credit-solution-1) of `ErrorBoundary` and `Suspense` has a significant implications on the user's experience.