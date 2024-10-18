# lis-simplelogger

Simple Logger for LIS.
Simultaneous setup for console logs and file log saves.

### Use Example

```python
from lis_simplelogger import LISSimpleLogger

FILEPATH="/my/path"
LIS_SL = LISSimpleLogger (
          log_file=f"{FILEPATH}/file.log",
          logger_name="my_logger"
        )

# this sets up the file and console logger to the specified path
LIS_SL.full_setup()

# file logger independent handling
file_logger = sl.get_file_logger()

file_logger.debug('This is a debug message')
file_logger.info('This is an informational message')
file_logger.warning('This is a warning message')
file_logger.error('This is an error message')
file_logger.critical('This is a critical message')

# console logger independent handling
console_logger = sl.get_console_logger()

console_logger.debug('This is a debug message')
console_logger.info('This is an informational message')
console_logger.warning('This is a warning message')
console_logger.error('This is an error message')
console_logger.critical('This is a critical message')
```

you can also use a comprehensive functions to log to both the file and the console.
```python
LIS_SL.info_log(msg)
LIS_SL.warning_log(msg)
LIS_SL.error_log(msg)
LIS_SL.critical_log(msg)
```
