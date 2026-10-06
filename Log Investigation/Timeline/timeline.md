timeline.md
# Authentication Investigation Timeline

| # | Timestamp | System        | Account | Event            | Source IP    |
| - | --------- | ------------- | ------- | ---------------- | ------------ |
| 1 | 08:31:12  | WORKSTATION01 | john    | Failed Login     | 192.168.1.50 |
| 2 | 08:31:18  | WORKSTATION01 | john    | Failed Login     | 192.168.1.50 |
| 3 | 08:31:25  | WORKSTATION01 | john    | Failed Login     | 192.168.1.50 |
| 4 | 08:31:31  | WORKSTATION01 | john    | Failed Login     | 192.168.1.50 |
| 5 | 08:31:39  | WORKSTATION01 | john    | Failed Login     | 192.168.1.50 |
| 6 | 08:31:46  | WORKSTATION01 | john    | Failed Login     | 192.168.1.50 |
| 7 | 08:31:53  | WORKSTATION01 | john    | Failed Login     | 192.168.1.50 |
| 8 | 08:32:04  | WORKSTATION01 | john    | Successful Login | 192.168.1.50 |

## Timeline Analysis

Seven failed authentication attempts occurred within approximately one minute.

The successful authentication occurred approximately 11 seconds after the final failed attempt.

This sequence is the primary reason the event requires additional investigation.

## Key Timeline Pattern

```text
07 Failed Logins
       ↓
Short Time Window
       ↓
Successful Login
       ↓
Potential Unauthorized Access
```

The pattern is suspicious but does not independently confirm compromise.