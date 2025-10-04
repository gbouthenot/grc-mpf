# Grc log coloriser for MPF / MPF-MC

## What is is

This is a coloriser script for [grc/grcat](https://github.com/garabik/grc)
that handles [Mission Pinball Framework](https://missionpinball.org) log
format.

Both the log file formats and the mpf live output are supported.

TESTED ON MPF 0.57 & MPF-MC 0.57

![Sample colorised output](/doc/output_colorised.png)

## Awaited log formats

```
(mpf) 2025-10-04 16:16:11,114 : INFO : EventManager : Event: ======'constellations_shots_complete'====== Args={'state': 'off'}
(mc)  2025-10-04 16:16:11,003 : EventManager : Event: ======'shutdown'====== Args={}
(live)           21:56:09.788 : INFO [EventManager] Event: ======'clear'====== Args={'key': 'service'}
```

## What it does

- Remove date
- Remove "Unordered handler for class" lines
- Colorise Date, log level, Class and sub-class

## Example use:
```shell
cat logs/2025-10-04-16-15-48-mpf-mpf2.log | grcat grc-mpf.conf | less -R
mpf both -Xt 2>&1 | grcat grc-mpf.conf
```

## Informations

Author: Gilles / Rebellion Pinball (misc@atomas.com)

Version 1.0 (2025-10-04)

Home: [project on Github](https://github.com/gbouthenot/grc-mpf)

## License

This project is released under the MIT License. Refer to the `LICENSE` file for details
