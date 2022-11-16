Lunaco is an anagram of `[lua] [con]ky [cal]endar`. It's a script to generate a customisable monthly calendar widget for conky. Recommended to use with a monospaced font.

Currently it seems some conky color tags add extra spaces which can mess with the formatting (especially for right and center), so use `--align-body=l` if using the `--today-color` and `--weekend-color` flags.

```
usage: lunaco.lua [-h] [options]

Lua script for a small conky calendar

options:
  -h, --help                show this help message and exit

  --align-body=<value>      set alignment of whole calendar
                            (default: c; options: c, l, r)
  --align-header=<value>    set alignment of calendar header
                            (default: c; options: c, l, r)
                            note: this is the only option
                            still active in combination with
                            the --no-format flag
  --color=<color>           set main text color (hex, omit #)
  --font-family=<font>      set font family (default:
                            Monospace)
  --header-color=<color>    color for header text (hex, omit
                            #)
  --hide-dow                hide days of week in the header
  --hide-month              hide the month in the header
  --hide-year               hide the year in the header
  --no-format               do not include any formatting
                            options
  --size=<num>              set font size (default: 11)
  --today-bold              set today's date in bold text
  --today-color=<color>     color for today's date (hex, omit
                            #)
  --weekend-color=<color>   color for weekend days (hex, omit
                            #)
```

**Include in your conky config file:**
```
${execpi 600 lua /path/to/lunaco.lua <options>}
```

**Example:**
```
${execpi 600 lua /path/to/lunaco.lua --today-bold --align-header=r --size=9}
```
