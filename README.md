
```

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase

$ npx create-next-app@latest
✔ What is your project named? … next-and-firebase
✔ Would you like to use TypeScript? … No / Yes
✔ Would you like to use ESLint? … No / Yes
✔ Would you like to use Tailwind CSS? … No / Yes
✔ Would you like to use `src/` directory? … No / Yes
✔ Would you like to use App Router? (recommended) … No / Yes
✔ Would you like to customize the default import alias (@/*)? … No / Yes
Creating a new Next.js app in /home/georgehill/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase.

Using npm.

Initializing project with template: default 


Installing dependencies:
- react
- react-dom
- next


added 21 packages, and audited 22 packages in 5s

3 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
Initialized a git repository.

Success! Created next-and-firebase at /home/georgehill/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase


~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase

$ ls
next-and-firebase

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase

$ cd next-and-firebase/

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ ls
jsconfig.json    node_modules  package-lock.json  README.md
next.config.mjs  package.json  public             src

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ npm run build

> next-and-firebase@0.1.0 build
> next build

   ▲ Next.js 14.1.4

 ✓ Linting and checking validity of types    
   Creating an optimized production build ...
 ✓ Compiled successfully
 ✓ Collecting page data    
 ✓ Generating static pages (3/3) 
 ✓ Collecting build traces    
 ✓ Finalizing page optimization    

Route (pages)                             Size     First Load JS
┌ ○ /                                     4.89 kB        82.9 kB
├   └ css/6b25432f67ef1376.css            1.75 kB
├   /_app                                 0 B              78 kB
├ ○ /404                                  181 B          78.2 kB
└ λ /api/hello                            0 B              78 kB
+ First Load JS shared by all             78.7 kB
  ├ chunks/framework-5429a50ba5373c56.js  45.2 kB
  ├ chunks/main-fe015bc011991627.js       31.8 kB
  └ other shared chunks (total)           1.76 kB

○  (Static)   prerendered as static content
λ  (Dynamic)  server-rendered on demand using Node.js


~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ npm install firebase

added 84 packages, and audited 106 packages in 7s

6 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ ls
jsconfig.json    node_modules  package-lock.json  README.md
next.config.mjs  package.json  public             src

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ pico src/pages/index.js 

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ cat src/pages/index.js 
import Head from "next/head";
import Image from "next/image";
import { Inter } from "next/font/google";
import styles from "@/styles/Home.module.css";

import { GoogleAuthProvider, signInWithCredential } from 'firebase/auth/web-extension';

const inter = Inter({ subsets: ["latin"] });

export default function Home() {
  return (
    <>
      <Head>
        <title>Create Next App</title>
        <meta name="description" content="Generated by create next app" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <link rel="icon" href="/favicon.ico" />
      </Head>
      <main className={`${styles.main} ${inter.className}`}>
        <div className={styles.description}>
          <p>
            Get started by editing&nbsp;
            <code className={styles.code}>src/pages/index.js</code>
          </p>
          <div>
            <a
              href="https://vercel.com?utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
              target="_blank"
              rel="noopener noreferrer"
            >
              By{" "}
              <Image
                src="/vercel.svg"
                alt="Vercel Logo"
                className={styles.vercelLogo}
                width={100}
                height={24}
                priority
              />
            </a>
          </div>
        </div>

        <div className={styles.center}>
          <Image
            className={styles.logo}
            src="/next.svg"
            alt="Next.js Logo"
            width={180}
            height={37}
            priority
          />
        </div>

        <div className={styles.grid}>
          <a
            href="https://nextjs.org/docs?utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
            className={styles.card}
            target="_blank"
            rel="noopener noreferrer"
          >
            <h2>
              Docs <span>-&gt;</span>
            </h2>
            <p>
              Find in-depth information about Next.js features and&nbsp;API.
            </p>
          </a>

          <a
            href="https://nextjs.org/learn?utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
            className={styles.card}
            target="_blank"
            rel="noopener noreferrer"
          >
            <h2>
              Learn <span>-&gt;</span>
            </h2>
            <p>
              Learn about Next.js in an interactive course with&nbsp;quizzes!
            </p>
          </a>

          <a
            href="https://vercel.com/templates?framework=next.js&utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
            className={styles.card}
            target="_blank"
            rel="noopener noreferrer"
          >
            <h2>
              Templates <span>-&gt;</span>
            </h2>
            <p>
              Discover and deploy boilerplate example Next.js&nbsp;projects.
            </p>
          </a>

          <a
            href="https://vercel.com/new?utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
            className={styles.card}
            target="_blank"
            rel="noopener noreferrer"
          >
            <h2>
              Deploy <span>-&gt;</span>
            </h2>
            <p>
              Instantly deploy your Next.js site to a shareable URL
              with&nbsp;Vercel.
            </p>
          </a>
        </div>
      </main>
    </>
  );
}

~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ npm run build

> next-and-firebase@0.1.0 build
> next build

   ▲ Next.js 14.1.4

 ✓ Linting and checking validity of types    
   Creating an optimized production build ...
request to https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap failed, reason: 

Retrying 1/3...
 ✓ Compiled successfully
   Collecting page data  ..(node:1043912) Warning: To load an ES module, set "type": "module" in the package.json or use the .mjs extension.
(Use `node --trace-warnings ...` to show where the warning was created)
/home/georgehill/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase/node_modules/@firebase/auth/dist/web-extension-esm2017/index.js:1
import { r as registerAuth, i as initializeAuth, a as indexedDBLocalPersistence, c as connectAuthEmulator } from './register-7b89e556.js';
^^^^^^

SyntaxError: Cannot use import statement outside a module
    at internalCompileFunction (node:internal/vm:77:18)
    at wrapSafe (node:internal/modules/cjs/loader:1288:20)
    at Module._compile (node:internal/modules/cjs/loader:1340:27)
    at Module._extensions..js (node:internal/modules/cjs/loader:1435:10)
    at Module.load (node:internal/modules/cjs/loader:1207:32)
    at Module._load (node:internal/modules/cjs/loader:1023:12)
    at cjsLoader (node:internal/modules/esm/translators:356:17)
    at ModuleWrap.<anonymous> (node:internal/modules/esm/translators:305:7)
    at ModuleJob.run (node:internal/modules/esm/module_job:218:25)
    at async ModuleLoader.import (node:internal/modules/esm/loader:329:24)
/home/georgehill/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase/node_modules/@firebase/auth/dist/web-extension-esm2017/index.js:1
import { r as registerAuth, i as initializeAuth, a as indexedDBLocalPersistence, c as connectAuthEmulator } from './register-7b89e556.js';
^^^^^^

SyntaxError: Cannot use import statement outside a module
    at internalCompileFunction (node:internal/vm:77:18)
    at wrapSafe (node:internal/modules/cjs/loader:1288:20)
    at Module._compile (node:internal/modules/cjs/loader:1340:27)
    at Module._extensions..js (node:internal/modules/cjs/loader:1435:10)
    at Module.load (node:internal/modules/cjs/loader:1207:32)
    at Module._load (node:internal/modules/cjs/loader:1023:12)
    at cjsLoader (node:internal/modules/esm/translators:356:17)
    at ModuleWrap.<anonymous> (node:internal/modules/esm/translators:305:7)
    at ModuleJob.run (node:internal/modules/esm/module_job:218:25)
    at async ModuleLoader.import (node:internal/modules/esm/loader:329:24)

> Build error occurred
Error: Failed to collect page data for /
    at /home/georgehill/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase/node_modules/next/dist/build/utils.js:1258:15 {
  type: 'Error'
}
   Collecting page data  .
~/Dropbox/GH Data (Dropbox)/Data 1 (Ind)/a Business, Current/ETDL/experiments/next-firebase/next-and-firebase

$ 
```

In the `pico` session initiated in the above terminal session, the only change that I made to `src/pages/index.js` was the addition of:

```
import { GoogleAuthProvider, signInWithCredential } from 'firebase/auth/web-extension';
```
 
