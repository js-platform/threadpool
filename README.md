# job.js

job.js provides pooling with web workers with a simple API to make web workers less scary to use.

With job.js, you can create a pool of web workers that you can accept work and run a callback when the work finishes:

````javascript
function add( a, b ) {
    console.log( 'adding ' + a + ' and ' + b );
    return a + b;
};

function go() {
    var pool = new job.Pool();
    pool.dispatch(
        add,
        [1, 2],
        function( result ) {
            console.log( result )
        }
    );
};
````

No need to worry about creating web workers or message passing. Notice that you can also log to the console!

# Contributing

Come find me on [irc.mozilla.org](http://irc.mozilla.org) in `#games` (my name is `ack`). I also love to accept pull requests.
