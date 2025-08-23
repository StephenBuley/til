# Curl Silent Show Errors

A colleague sent a curl command today to test out an api and it had some of the usual options on the command, but ones I hadn't run into before and wanted to look up were this:

```bash
curl -sS
```

The `-s, --silent` means curl won't output the progress bar or errors, only the actual output of the requested data. The `-S, --show-error` flag can be used in conjunction to flip only the showing errors portion back on. So essentialy, `curl -sS` means "Don't show me the progress bar, but do tell me if any errors occur." Neat!
