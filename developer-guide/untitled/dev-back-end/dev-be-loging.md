# Dev - BE - logger

## Import

This package is located in `src/logger`, typically imported through

```text
import {d, i, w, e} from '<path_to>/src/logger';
```

## Usage

logging can be done as follows :-

```text
d(`this is a debug log`);
i(`this is an info log`);
w(`this is a warn log`);
e(`this is an error log`);
```

resulting in the following in the console

```text
[04-11-2020 07:01:34 am] - DEBUG - this is a debug log
[04-11-2020 07:01:34 am] - INFO  - this is an info log
[04-11-2020 07:01:34 am] - WARN  - this is a warn log
[04-11-2020 07:01:34 am] - ERROR - this is an error log
```

Extra arguments can be passed to the log as well eg

```text
d(`this is a debug log`, obj1, ...);
i(`this is an info log`, obj2, ...);
w(`this is a warn log`, obj3, ...);
e(`this is an error log`, obj4, ...);
```



