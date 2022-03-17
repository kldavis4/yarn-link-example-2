# Reproduction example for 

## Setup

`git clone https://github.com/tinacms/tinacms.git`

`git clone https://github.com/kldavis4/yarn-link-example`

`cd tinacms && git checkout 7a5e47394a7e6c59cb7cd5e00358aa7331bd67ad && yarn && cd ..`

`cd yarn-link-example && yarn`

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

Note: If you move the `@tinacms/graphql` dependency to the root package.json, you get this more helpful error:

```
Cannot link @tinacms/graphql into yarn-link-example@workspace:. dependency fs-extra@npm:9.1.0 conflicts with parent dependency fs-extra@npm:10.0.0
```
