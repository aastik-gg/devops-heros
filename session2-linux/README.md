## Difference Between Soft Link and Hard Link

| Soft Link                                         | Hard Link                                                                       |
| ------------------------------------------------- | ------------------------------------------------------------------------------- |
| Points to the filename/path of the target object. | Points directly to the inode of the target object.                              |
| Breaks if the original object is deleted.         | Continues to access the original data even if the original filename is deleted. |

**Soft Link:**

```bash
ln -s target linkName
```

**Hard Link:**

```bash
ln target linkName
```

---

## `adduser` vs `useradd`

### `useradd`

`useradd` is a native, low-level command used to create user accounts. It performs only the basic account creation tasks and is generally non-interactive.

By default, it may not create a home directory or set a password, so additional options or commands may be required to configure the account fully.

**Best suited for:** Automation, shell scripts, and situations where precise control over configuration is required.

### `adduser`

`adduser` is a high-level, user-friendly wrapper around `useradd`. It provides an interactive, step-by-step process for creating a user.

It can automatically:

* Create a home directory
* Assign a standard shell
* Prompt for a password
* Set up appropriate permissions and profile files

**Best suited for:** Manual and everyday user creation, especially on Ubuntu and Debian-based systems.

### In short

**`useradd` →** Low-level, non-interactive, precise control
**`adduser` →** High-level, interactive, user-friendly

---

## `journalctl`

`journalctl` is the central command used to view system and application logs in modern Linux. It allows you to search and analyze logs collected by the system's journal.

Instead of manually checking multiple log files, `journalctl` provides a single interface for viewing system events, errors, and service messages.

### Common Commands

**View all logs:**

```bash
journalctl
```

**Watch logs live:**

```bash
journalctl -f
```

**Check logs for a specific service:**

```bash
journalctl -u service
```

**View the current user's journal:**

```bash
journalctl --user
```
