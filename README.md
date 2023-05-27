# ⚙️ svg2avd

> Kotlin script to convert SVG files to **A**ndroid **V**ector **D**rawables.

### Usage

```bash
./svg2avd.main.kts --help
```

```
Usage: svg2avd.main.kts [OPTIONS]

  ⚙️ svg2avd: Convert SVG files to Android Vector Drawables (AVD).

Options:
  -i, --input PATH     SVG assets input directory
  -o, --output PATH    AVD assets output directory
  -p, --precision INT  Set number of digits in the fractional part (svgo)
  -q, --quiet          Print errors only
  -h, --help           Show this message and exit
```

### Example

```bash
./svg2avd.main.kts --input=icons 
```

```
⚙️ Converting icons/alarm.svg to icons/alarm.xml
⚙️ Converting icons/delete.svg to icons/delete.xml
⚙️ Converting icons/lightbulb.svg to icons/lightbulb.xml

✅ /home/svg2avd/icons
```

### SVG compression with [svgo](https://github.com/svg/svgo)

```bash
./svg2avd.main.kts --input=icons --precision=2
```

```
Processing directory '/home/svg2avd/icons':


alarm.svg:
Done in 17 ms!
0.386 KiB - 17% = 0.32 KiB

delete.svg:
Done in 3 ms!
0.21 KiB - 9.8% = 0.189 KiB

lightbulb.svg:
Done in 4 ms!
0.288 KiB - 11.9% = 0.254 KiB

⚙️ Converting /tmp/alarm.svg to icons/alarm.xml
⚙️ Converting /tmp/delete.svg to icons/delete.xml
⚙️ Converting /tmp/lightbulb.svg to icons/lightbulb.xml

✅ /home/svg2avd/svg2avd/icons
```

### Credits

- [com.android.tools:sdk-common](https://maven.google.com/web/index.html?q=sdk-common#com.android.tools:sdk-common)
  > sdk-common library used by other Android tools libraries.
- [ajalt/clikt](https://github.com/ajalt/clikt)
  > Multiplatform command line interface parsing for Kotlin
- [svg/svgo](https://github.com/svg/svgo)
  > Node.js tool for optimizing SVG files
- [jakearchibald/svgomg](https://jakearchibald.github.io/svgomg/)
  > Web GUI for SVGO
- [google/material-design-icons](https://github.com/google/material-design-icons)
  > Material Design icons by Google
