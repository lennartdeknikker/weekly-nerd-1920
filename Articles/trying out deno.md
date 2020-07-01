# Trying out Deno.js
**Lennart de Knikker | July 1st 2020**

![deno logo](https://github.com/lennartdeknikker/weekly-nerd-1920/blob/master/assets/images/deno/deno.png)

Since I'm subscribed to the DEV Digest newsletter I received one a month ago which contained an interesting link to [this article](https://dev.to/aralroca/learn-deno-chat-app-37f0). I had also heard about Deno.js on [the Syntax podcast](https://syntax.fm/) by Wes Bos and Scott Tolinski. They were quite excited about this new runtime for JavaScript and TypeScript. The article in the newsletter provided a tutorial to get acquainted with the most important Deno features:

- permissions
- deno commands
- how to use deno internals
- the use of third-party dependencies
- serving files
- websockets
- formatting files
- testing
- debugging

After following this tutorial, I decided to do some more research about Deno and try to find out why it's there, how it compares to NodeJS and in what cases it would be nice to use.

## About Deno
Interestingly Deno was created by the same person that created nodeJS, Ryan Dahl. He did so, because according to him there are some flaws to nodeJS, which Deno tries to solve.

Deno is a new JavaScript runtime. In june 2018 Deno was announced at JSConf. It has only been around for two years now, which means that in comparison to nodeJS which was was first released in 2011 it's still very new.[(1)][1]

In the video where Ryan Dahl announced Deno, he ended with a disclaimer[(2)][2]: 
> "Ignore this talk- **use Node**. Node isn't going anywhere!

In a video by [Academind](https://academind.com/), a company founded by Maximilian Schwarzmüller and Manuel Lorenz, Schwarzmüller draws this conclusion[(3)][3]:

> "You could say Deno is not released aiming to replace NodeJS. It's just that for some applications it might be a better choice to use Deno."



## NodeJS vs Deno

### Advantages
#### Typescript support
Deno does not only support JavaScript, it also out of the box supports Typescript without the need for any additional compilers.[(4)][4]

#### URL imports
With Deno you don't need to install packages or import modules. You can import packages using a url like this:
```js
import serve from 'https://deno.land/std@0.50.0/http/server.ts'
```
This difference means there's no need for a `package.json` file and it's easier to see where a certain package or imported module comes from.

One of the bigger advantages of URL imports which is a direct result is that there's no need for a `node_modules` folder anymore as well.[(5)][5]

#### Top level await
Another feature that makes Deno different from NodeJS is that you can use await statements at the top level. Any experienced programmer who uses asynchronous javaScript has sometimes been forced to wrap code in a function, just to be able to use `async await`. In Deno this is not necessary anymore.[(6)][6]

#### better security
In nodeJS any script can run a server or make changes to your files, without any easy option for blocking this. In Deno third-party modules can not run anything harmful. By default scripts have no permissions. By adding flags like `--allow-net` it's possible to for example allow network access. A script that's run with this flag can still not change any files unless you also add a flag for that. This way, it's much easier to control those permissions than it is in NodeJS.[(7)][7]

### Disadvantages
Because Deno is very new. It's not completely stable yet. As stated on their website there are still some big limitations. On their website they seem to be completely transparent about these problems and summed them up theirselves[(8)][8]:

- Deno is not compatible with existing javascript tooling and NPM packages
- HTTP Server Performance is worse than it is in NodeJS. They are still optimizing and hoping to achieve better results in the future.
- The typescript compiler Deno uses now is very slow. For that to get much faster, they will need to port their compiler to Rust, which will not happen any time soon.
- Their plugin system is still unstable





## How do I use Deno?
I recommend [this tutorial](https://dev.to/aralroca/learn-deno-chat-app-37f0) written by Aral Roca on dev.to if you're interested to try out Deno yourself. It's a step by step guide for building a simple chat application. The differences with nodeJS are all explained in detail along the way.

## What I learned
Deno is a very interesting, but nascent project, which has a lot of potential, but as mentioned above, it still has some major flaws, which will just take time to get solved. It was fun to get some hands on experience with this new runtime and I will continue to keep track of their progress. NodeJS will still be the more stable and better choice for most projects, but if you want to build some simple application that will not have a lot of people depending on it, I recommend to give it a try.

## Sources
1. https://nodejs.org/dist/
2. https://www.youtube.com/watch?v=M3BM9TB-8yA
3. https://www.youtube.com/watch?v=3Vl8a3zYjiw
4. https://deno.land/v1
5. https://medium.com/@griko/i-made-a-deno-module-registry-using-next-js-vercel-and-github-6954d308e1e2
6. https://www.youtube.com/watch?v=3Vl8a3zYjiw
7. https://medium.com/deno-tutorial/deno-security-65af9811d9c9
8. https://deno.land/v1

[1]: https://nodejs.org/dist/
[2]: https://www.youtube.com/watch?v=M3BM9TB-8yA
[3]: https://www.youtube.com/watch?v=3Vl8a3zYjiw
[4]: https://deno.land/v1
[5]: https://medium.com/@griko/i-made-a-deno-module-registry-using-next-js-vercel-and-github-6954d308e1e2
[6]: https://www.youtube.com/watch?v=3Vl8a3zYjiw
[7]: https://medium.com/deno-tutorial/deno-security-65af9811d9c9
[8]: https://deno.land/v1