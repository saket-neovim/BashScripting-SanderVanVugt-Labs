# Bash Scripting Course Exercises

Personal practice scripts from Sander van Vugt's Bash scripting labs. The original course provides the learning context; this repository records exercise implementations and variations, not the course material or a supported administration toolkit.

## Exercise guide

| File | Focus |
| --- | --- |
| [lab6](lab6) | Install a package and enable a same-named service |
| [lab6.2](lab6.2) | Choose a package manager from OS information |
| [lab7](lab7) | Rename matching text files in the current directory |
| [lab8](lab8), [lab8.2](lab8.2) | Inspect disk and memory thresholds |
| [lab9](lab9) | Loop over package/service arguments with a memory check |

## Requirements and checks

Use Bash on a disposable Linux VM. Package exercises assume `apt` or `yum`, service exercises assume systemd, and resource checks use Linux `df`/`free` output.

```bash
bash -n lab6 lab6.2 lab7 lab8 lab8.2 lab9
```

This checks syntax without executing commands. Read the chosen script before running it: package/service exercises use `sudo`, `lab7` renames files, and `lab8` assumes a particular disk device. A package name is not always its service name.

## Limitations and cleanup

These short exercises retain their original learning assumptions and need stronger input/error handling before reuse outside a lab. There is no committed runtime test evidence. Use synthetic files, record what was changed, and reverse package/service or file changes in the disposable environment afterward. Keep credentials and local environment files out of Git.
