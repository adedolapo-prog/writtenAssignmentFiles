## What is setTimeOut()?

SetTimeOut is a function which delays the execution of another function by the milliseconds specified in the setTimeOut function. The setTimeOut function accepts two parameters which are the function to be delayed and the milliseconds to delay it by.

Let us look at how the setTimeOut function works.

    setTimeOut(function,milliseconds); is generally how it is written.

Here is an example of the setTimeOut function.

    setTimeOut(() => {alert 'hello,world'},3000); //This alerts hello world on the page after 3 seconds.

## What are promises in Javascript?

A javascript promise contains both a producing code which takes some time to execute and a consuming code which waits for the result from the producing code.

## WHat are side effects in programming?

Side effects are application state changes that are observed outside a called function aside from its return value. It is said that writing pure functions in javascript is a better synthax than writing functions with side effects. A pure function is one that has the same output every time a particular input is given and also a function with no side effects. Side effects generally alter the external state of the function. It could be altering a global variable and so on.

Side effects include:

- logging to the console
- modifying an external variable
- writing to a file
- writing to a network
- triggering an external process

Here is an example of a side effect:

    const series = {
        name: 'Naruto',
        episodes: 972,
        currentEpisode: 320,
    };

    const watchedEpisodes = () => {
        series.currentEpisode = series.currentEpisode++;
    };

Each time the watchedEpisodes function is called, it increases the number of currentEpisode by 1 and the currentEpisode is an object property for series. Therefore, this is a side effect.

A way to solve this is by declaring a new variable within the scope of the function which would be the one altered and not the object property.

    const watchedEpisodes = () => {
        let latestEpisode = series.currentEpisode;
        return latestEpisode++;
    };

This assigns the altered value to latestEpisode while current episode remains intact.
