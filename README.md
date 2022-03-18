# Reproduction example for 

## Setup

`git clone git@github.com:kldavis4/tinacms.git`

`git clone https://github.com/kldavis4/yarn-link-example-2`

`cd tinacms && git checkout cf349699f66895beeee9a4b2d3710bfec5ce02bb && yarn && cd ..`

`cd yarn-link-example-2 && yarn`

## Reproduction

```
➤ YN0000: ┌ Fetch step
➤ YN0000: └ Completed in 0s 492ms
➤ YN0000: ┌ Link step
➤ YN0001: │ Error: Assertion failed: Writing attempt prevented to /Users/kldavis/projects/tinacms-yarn-link-repro/packages/@tinacms/cli/node_modules/@tinacms/graphql which is outside project root: /private/tmp/yarn-link-example-2
    at fb (/private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:712:1725)
    at nce (/private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:712:2298)
    at T_e (/private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:712:6802)
    at rce.finalizeInstall (/private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:697:26714)
    at runMicrotasks (<anonymous>)
    at processTicksAndRejections (internal/process/task_queues.js:97:5)
    at async ze.linkEverything (/private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:441:14959)
    at async /private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:444:4324
    at async Je.startSectionPromise (/private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:413:3303)
    at async ze.install (/private/tmp/yarn-link-example-2/.yarn/releases/yarn-3.2.0.cjs:444:4100)
➤ YN0000: └ Completed in 1s 843ms
```
