# Eris Logger

Eris logging package is a fork of the [logrus](https://github.com/Sirupsen/logrus) logger with the `ErisFormatter` set by default.

It also avoids logrus' shortcoming of not able to ignore logging levels set by the package's `SetLevel()` function.

## Generic Initialization

```
import log "github.com/eris-ltd/eris-logger"

log.SetLevel(log.WarnLevel)
if do.Verbose {
  log.SetLevel(log.InfoLevel)
} else if do.Debug {
  log.SetLevel(log.DebugLevel)
}

```

## Initialization for tests

```
import log "github.com/eris-ltd/eris-logger"

log.SetLevel(log.ErrorLevel)
// log.SetLevel(log.InfoLevel)
// log.SetLevel(log.DebugLevel)
```
