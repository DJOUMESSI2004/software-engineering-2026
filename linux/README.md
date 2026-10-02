# Linux

## What I am learning

How software actually runs on a machine: files, processes, services, permissions, logs, and networking, all from the command line.

## Why it matters

Every later topic runs on Linux. Docker containers are Linux processes, cloud servers are Linux machines, and Kubernetes nodes are Linux hosts. If I cannot operate and debug Linux, I cannot debug anything built on top of it.

> **Goal:** be comfortable operating and debugging a Linux machine from the command line.

---

## Learning objectives

By the end of this topic I can:

- Navigate the filesystem and explain the main directories (`/etc`, `/var`, `/home`, `/tmp`, `/usr`)
- Combine commands with pipes and redirection
- Explain what a process is and inspect, signal, and stop processes
- Manage services with `systemd`
- Read and change permissions, and manage users and groups
- Read logs and filter them for evidence
- Inspect network state: ports, connections, DNS
- Write Bash scripts that are safe and readable
- Debug a service that fails to start or cannot be reached

---

## Weekly progression

| Week | Focus | Key commands |
|---|---|---|
| 1 | Filesystem, files, pipes, redirection, permissions | `ls` `cd` `cp` `mv` `rm` `find` `grep` `less` `tail` `chmod` `chown` |
| 2 | Processes, services, logs, environment variables, users and groups | `ps` `top` `kill` `systemctl` `journalctl` `env` `export` `useradd` |
| 3 | Networking and troubleshooting, Bash scripting | `ss` `curl` `ping` `dig` `df` `du` `free`, scripts, exit codes |
| 4 | Mini-project and review | Server Health Monitor, weekly reviews |

---

## Checklist

- [ ] Navigate the filesystem
- [ ] Understand absolute and relative paths
- [ ] Use pipes
- [ ] Redirect output
- [ ] Search files and text (`find`, `grep`)
- [ ] Understand processes
- [ ] Inspect ports
- [ ] Understand permissions (`rwx`, octal)
- [ ] Manage users and groups
- [ ] Manage services
- [ ] Read logs
- [ ] Monitor CPU, memory, and disk
- [ ] Write Bash scripts (variables, conditions, loops, functions, exit codes)
- [ ] Debug a service

A box is ticked only when I can do or explain the task without relying entirely on a tutorial.

---

## Exercises

Small focused tasks that answer: *can I actually do this?*

- [ ] Create a Bash script that takes an argument and validates it
- [ ] Find the process using a given port and stop it
- [ ] Fix a file that a user cannot read because of permissions
- [ ] Find the 10 largest files under a directory
- [ ] Extract all error lines from a log within a time window
- [ ] Create a user, add them to a group, and restrict a directory to that group
- [ ] Create and enable a small `systemd` service

## Labs

Investigation-oriented. Each lab ends with a written note: symptom, evidence, hypothesis, root cause, fix, lesson.

- [ ] **App is running but unreachable:** investigate, find the root cause, fix it, document it
- [ ] **Service fails to start:** read the journal, find the cause (permissions, path, environment variable, port conflict)
- [ ] **Disk full:** find what filled it and clean up safely
- [ ] **Slow machine:** identify which process is consuming CPU or memory

## Mini-project: Server Health Monitor

A Bash script that reports CPU, memory, disk usage, key processes, and service status.

Requirements:

- Clear output, and non-zero exit code when a threshold is exceeded
- Configurable thresholds through environment variables
- Logs to a file
- Its own README, versioned in Git with a clean commit history

---

## Resources

- *The Missing Semester of Your CS Education* (shell, scripting, command line)
- Linux manual pages (`man`, `--help`, `tldr`)
- Official `systemd` documentation

## Completion criteria

- [ ] I can explain every checklist item in my own words
- [ ] I can complete common tasks without a tutorial
- [ ] I can debug a basic service failure using the debugging methodology
- [ ] The mini-project is delivered with a README
- [ ] I reviewed the key concepts without AI
- [ ] Weekly reviews are written