# Reproduction example for 

## Setup

`git clone git@github.com:kldavis4/tinacms.git`

`git clone https://github.com/kldavis4/yarn-link-example-2`

`cd tinacms && git checkout cf349699f66895beeee9a4b2d3710bfec5ce02bb && yarn && cd ..`

`cd yarn-link-example-2 && yarn`

## Reproduction

```
yarn link ../tinacms -rp

➤ YN0000: ┌ Resolution step
➤ YN0000: └ Completed
➤ YN0000: ┌ Fetch step
➤ YN0000: └ Completed in 0s 252ms
➤ YN0000: ┌ Link step
➤ YN0001: │ Error: Assertion failed: Writing attempt prevented to /path/to/tinacms/packages/@tinacms/graphql/node_modules/fs-extra which is outside project root: /path/to/projects/yarn-link-example
    at $0 (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:695:1626)
    at Bce (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:695:2199)
    at T6e (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:695:6703)
    at yce.finalizeInstall (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:680:26260)
    at async Ke.linkEverything (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:441:14966)
    at async /Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:444:4329
    at async Fe.startTimerPromise (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:412:3730)
    at async Ke.install (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:444:4105)
    at async /Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:514:1744
    at async Function.start (/Users/kldavis/projects/example/.yarn/releases/yarn-3.1.1.cjs:412:2287)
➤ YN0000: └ Completed in 0s 306ms
➤ YN0000: Failed with errors in 0s 738ms
```
