# What I've learnt
###### *For more details, see [`src/exercise/*.md`](https://github.com/HelpMe-Pls/react-suspense/tree/master/src/exercise) files*
-------------

## Simple Data-fetching
- Use `Suspense` in conjunction with `ErrorBoundary` ([at 2:00](https://epicreact.dev/modules/react-suspense/simple-data-fetching-extra-credit-solution-1)) to handle runtime errors as well as errors while fetching data. 
- SoC by abstracting data fetching handlers [into a module](https://epicreact.dev/modules/react-suspense/simple-data-fetching-extra-credit-solution-3).  


## Render as you fetch
- Imagine when your app loads, you need some data **before** you can show anything useful. The best approaches to using [`Suspense`](https://reactjs.org/docs/react-api.html#reactsuspense) involve kicking off the request for the data *as soon as* you have the information you need for the request ([at 1:25](https://epicreact.dev/modules/react-suspense/suspense-image-extra-credit-solution-2)). This is called the “[**Render as you fetch**](https://github.com/HelpMe-Pls/react-suspense/blob/master/src/examples/fetch-approaches/render-as-you-fetch.js)” approach.
- [The positioning](https://epicreact.dev/modules/react-suspense/render-as-you-fetch-extra-credit-solution-1) of `ErrorBoundary` and `Suspense` has a significant implications on the user's experience.
- [Transitions](https://reactjs.org/blog/2022/03/29/react-v18.html#new-feature-transitions) are a new concurrent feature introduced in React 18. They allow you to mark updates as transitions, which tells React that they can be interrupted and avoid going back to Suspense fallbacks for already visible content.

## Cache resources
- Implement simple caching with `context` ([at 2:25](https://epicreact.dev/modules/react-suspense/cache-resources-extra-credit-solution-2)). 
- Implement cache invalidation to re-fetch stale data ([at 2:00](https://epicreact.dev/modules/react-suspense/cache-resources-extra-credit-solution-3)).

## Suspense Image
- What if your UI doesn’t look any good *until* the image is actually loaded? Or what if you want to render a fallback in the image’s place *while it’s loading* (you want to provide *your own* loading UI)?
- In that case, with `Suspense`, we have an opportunity to make this experience a lot better. We have two related options:
1. Make an `<Img/>` component that suspends until the **browser** has actually preloaded the image ([at 2:15](https://epicreact.dev/modules/react-suspense/suspense-image-solution)).
2. Make a request for the image alongside the data ([at 1:25](https://epicreact.dev/modules/react-suspense/suspense-image-extra-credit-solution-1)), then utilizing the benefits of "[render as you fetch](https://epicreact.dev/modules/react-suspense/suspense-image-extra-credit-solution-2)".

# Suspense with a custom hook
- Abstracting away the fetching, caching and `Suspense`'s logic into a reusable [custom hook](https://epicreact.dev/modules/react-suspense/suspense-with-a-custom-hook-extra-credit-solution-1) to make your code more declarative.

