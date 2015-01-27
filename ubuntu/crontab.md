# crontab

```text
MIN HOUR DOM MON DOW CMD
```

**Note**
Cron job can't be used to schedule a task to execute every second.

| Field | Description | Allowed Value |
| ----- | ----------- | ------------- |
| MIN | Minute field | 0-59 |
| HOUR | Hour field | 0-23 |
| DOM | Day of Month | 1-31 |
| MON | Month field | 1-12 |
| DOW | Day Of Week | 0-6 |
| CMD | Command | Any command to be executed. |

| Keyword | Equivalent |
| ------- | ---------- |
| @yearly | 0 0 1 1 * |
| @daily | 0 0 * * * |
| @hourly | 0 * * * * |
| @reboot | Run at startup. |

### To view cron jobs

```bash
$ crontab -l
```

### To edit cron jobs

```bash
$ crontab -e
```

### Schedule to execute at a specific time

```bash
30 08 10 06 * CMD
```

### Schedule to execute more than once

```bash
00 11,16 * * * CMD
```

To execute at 11:00 and 16:00

### Schedule to execute at a specific range of time

```bash
00 09-18 * * * CMD
```

To execute between 9:00 and 18:00

### Schedule to execute every minute

```bash
$ * * * * * CMD
```

### Schedule to execute every 10 minutes

```bash
$ */10 * * * * CMD
```

### Schedule to execute every year using special keyword

```bash
$ @yearly CMD
```
