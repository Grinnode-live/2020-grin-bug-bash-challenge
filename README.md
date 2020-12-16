# Grinnode.live Winter 2020 Bug Bash Challenge and free GRIN/BTC prizes giveaway

[Grin](https://grin.mw/) is a privacy-preserving digital currency built openly by developers distributed all over the world. We are approaching a [Grin v5.0.0 network upgrade (Hard Fork 4: January 2021)](https://forum.grin.mw/t/grin-v5-0-0-network-upgrade-hard-fork-4-january-2021/7895) and we want to improve on node and wallet stability by performing as large number of tests as possible. For this, we need your help! We are ready to offer prizes and giveways for those who find bugs in Grin!

## How to participate?

This section describes the overall protocol.

### Preparing environment

1. Properly setup GitHub and KeyBase accounts. Make sure your KeyBase points to same GitHub account as one that authored the gist bug reports!
2. You can build and run the [node](https://github.com/mimblewimble/grin) as described [here](https://github.com/mimblewimble/docs/wiki/How-to-run-a-Grin-node). Check [official documentation](https://docs.grin.mw/) if you want to know more.
3. You can build and run the [wallet](https://github.com/mimblewimble/grin-wallet), if you want to test transaction you might need more than one local instance of the wallet.
4. Some grin coins! Let us know on the KeyBase team channel if you need some to get your tests going.
5. Check which tests are ready by opening our [issue tracker](https://github.com/Grinnode-live/2020-grin-bug-bash-challenge/issues) and using query `is:issue is:open no:assignee label:ready-for-test` or just click [here](https://github.com/Grinnode-live/2020-grin-bug-bash-challenge/issues?q=is%3Aissue+is%3Aopen+no%3Aassignee+label%3Aready-for-test). Do NOT assign to yourself more than one issue simultaneously!
4. A lot of patience! 

### Performing the test

Follow the test description from the assigned GitHub issue. Use your local environment to run the test case. Make sure you gather enough data for your report, we would need at least the following

1. Description of all the steps with as many details as possible. Do it in a form of `README.md` file.
2. Node/Wallets debug logs with links to specific lines and your comments to each line indicating the meaning of the log line. All log files should be set to `== debug` mode to provide sufficient level of details.
3. Precise information about your test environment (operating system, build environment etc)

Once you are done and gathered sufficient amount of data so that your test could be reproducible by someone else, wrap it all up in a single [secret gist repository](https://gist.github.com/). This would allow you to link a specific line of the logs. If your output log is too long gist might not allow you to link a specific line, in such case make sure you have a copy of specific line with the comment and line number ready for your report.

### Reporting passing test

If everything went as planned comment on the test issue that you are assigned to and add a `ready-for-review` label to it and you can assign yourself a different issue at this stage if you want. We will look into it, we might ask you to provide additional information or change something in your test if it wasn't executed properly. Once review is done we will assign `ready-for-reward` label to it and close it. The congratulations! You will officially get paid for testing a feature!

### How to report the bug

If the result is not as expected before you report a bug make sure you performed the test properly. Incorrect results resulting from incorrect usage are not bugs!

Reporting the bug case is more tricky, as bugs are potential security vulnerabilities we do not want your report to go public. In such case please provide the link to your secret gist to @marekyggdrasil via KeyBase in a private message. We will attempt to reproduce your bug and if we succeed you will be paid for the bug report.

### How to claim your prize

Rewards will be distributed once the challenge is officially over (add end date here).

1. We will keep track of who run which tests, but we are only human... So provide us with your list just for double check!
2. Once everything checks out, we will reach you requesting your payment details (request BTC address / or provide GRIN transaction file, depending on the payment)
3. After transaction is completed we will include the transaction proof at the end of the issue and add a label to `rewarded` to it. Ka-ching!!!

## Prizes / Free giveaways

| Task               | Condition                                                                                                   | Prize                                       |
|--------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Testing a feature. | Properly documenting the procedure, providing logs and highlighting relevant outputs, describing procedure. | 10€                                         |
| Finding a bug.     | As above + we manage to reproduce it.                                                                       | 50€-500€ (depending on severity of the bug) |
| First prize.       | Owner of github account who tested and documented most features.                                            | 500€                                        |
| Second prize.      | Second to the one above.                                                                                    | 250€                                        |
| Third prize.       | You get it... ;)                                                                                            | 125€                                        |

We will only attempt to reproduce the bug reports. As for remaining tests we will only briefly review the log outputs. We assume users would not attempt to forge successful tests as bugs are paid a lot more.

## Why are we doing this?

We want Grin stack to get more stable. It could use a solid amount of integration tests. We also believe that it is an excellent approach to promote Grin.

## FAQ

### What if I find a bug / vulnerability that is not listed in the test cases? For example, a bug discovered during while setting up the test environment?

By all means please report it to us and if we reproduce it you will be rewarded for it! Just keep in mind your report might be take us longer to reproduce as we haven't prepared a protocol for it.

### How to enable DEBUG mode for log files?

Edit your `grin-server-toml` and/or `grin-wallet.toml` file and make the following changes:
```
#log level for file: Error, Warning, Info, Debug, Trace
file_log_level = "Debug"
```

### How can I donate to this challenge?
Please use the Grinnode.live donation addresses only: https://github.com/Grinnode-live/grinnode.live/blob/master/donation.md

### Can I add a test case?
Yes, we are encouraging you to do so. Just open an issue on https://github.com/Grinnode-live/2020-grin-bug-bash-challenge/issues and you created a test-case. Please do not assign `ready-for-test` label, this is how we keep track of that needs to be changed.
