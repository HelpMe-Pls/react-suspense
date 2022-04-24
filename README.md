# What I've learnt
###### *For more details, see [`src/exercise/*.md`](https://github.com/HelpMe-Pls/react-suspense/tree/master/src/exercise) files*
-------------

## Simple Data-fetching
- Use `Suspense` in conjunction with `ErrorBoundary` ([at 2:00](https://epicreact.dev/modules/react-suspense/simple-data-fetching-extra-credit-solution-1)) to handle runtime errors as well as errors while fetching data. 
- SoC by abstracting data fetching handlers [into a module](https://epicreact.dev/modules/react-suspense/simple-data-fetching-extra-credit-solution-3).  


## Render as you fetch
- Imagine when your app loads, you need some data **before** you can show anything useful. The best approaches to using [`Suspense`](https://reactjs.org/docs/react-api.html#reactsuspense) involve kicking off the request for the data *as soon as* you have the information you need for the request. This is called the “[**Render as you fetch**](https://github.com/HelpMe-Pls/react-suspense/blob/master/src/examples/fetch-approaches/render-as-you-fetch.js)” approach.
- [The positioning](https://epicreact.dev/modules/react-suspense/render-as-you-fetch-extra-credit-solution-1) of `ErrorBoundary` and `Suspense` has a significant implications on the user's experience.
- [Transitions](https://reactjs.org/blog/2022/03/29/react-v18.html#new-feature-transitions) are a new concurrent feature introduced in React 18. They allow you to mark updates as transitions, which tells React that they can be interrupted and avoid going back to Suspense fallbacks for already visible content.
- Implement cache invalidation to re-fetch stale data ([at 2:00](https://epicreact.dev/modules/react-suspense/cache-resources-extra-credit-solution-3)).