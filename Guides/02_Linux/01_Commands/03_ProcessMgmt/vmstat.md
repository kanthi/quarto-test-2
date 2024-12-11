# vmstat

`vmstat` (Virtual Memory Statistics) is a powerful Linux command that provides information about system processes, memory, paging, block IO, traps, and CPU activity.

## Basic Syntax

```bash
vmstat [options] [delay [count]]
```

## Common Options

- `-a` : Display active and inactive memory
- `-f` : Display the number of forks since boot
- `-m` : Display memory information in MB rather than KB
- `-n` : Display header only once
- `-s` : Display memory statistics
- `-d` : Display disk statistics

## Example Output

```bash
$ vmstat
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 1  0      0 823012  66268 460644    0    0     1     1    1    2  1  0 98  0  0
```

## Field Descriptions

### Procs
- `r`: Number of processes waiting for runtime
- `b`: Number of processes in uninterruptible sleep

### Memory
- `swpd`: Used virtual memory
- `free`: Idle memory
- `buff`: Memory used as buffers
- `cache`: Memory used as cache

### Swap
- `si`: Memory swapped from disk
- `so`: Memory swapped to disk

### IO
- `bi`: Blocks received from block device
- `bo`: Blocks sent to block device

### System
- `in`: Number of interrupts per second
- `cs`: Number of context switches per second

### CPU
- `us`: Time spent in user code
- `sy`: Time spent in system code
- `id`: Time spent idle
- `wa`: Time spent waiting for IO
- `st`: Time stolen from a virtual machine

## Example with Delay

```bash
$ vmstat 2 5  # Display stats every 2 seconds, 5 times
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 1  0      0 823012  66268 460644    0    0     1     1    1    2  1  0 98  0  0
 0  0      0 823012  66268 460644    0    0     0     0   88  156  1  0 99  0  0
 0  0      0 823012  66268 460644    0    0     0     0   85  152  0  0 100 0  0
 0  0      0 823012  66268 460644    0    0     0     0   86  154  0  0 100 0  0
 0  0      0 823012  66268 460644    0    0     0     0   84  150  0  0 100 0  0
```

This command is particularly useful for:
- System performance monitoring
- Troubleshooting memory issues
- Identifying system bottlenecks
- Real-time system statistics