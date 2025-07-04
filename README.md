# Sentry Cron reporter

Package to send reports to https://sentry.io/crons/ service.

Handles stop, start and detects and sends crash too.

For more information see https://docs.sentry.io/product/crons/ and https://docs.sentry.io/product/crons/getting-started/http/


## Example

```go
package main

import "github.com/teamniteo/go-sentry/cron"

var cronReport = cron.NewMonitor("teamniteo", "monitor-slug-or-uuid")

func main() {
    cronReport.Start()
    defer cronReport.Stop() // will handle crash too

    // ... the rest of the stuff
}

```

## We're hiring!

At Niteo we regularly contribute back to the Open Source community. If you do too, we'd like to invite you to [join our team](https://niteo.co/careers)!
