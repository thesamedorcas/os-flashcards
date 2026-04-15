# Operating Systems Flashcards

My personal exam prep tool for the Operating Systems module. An interactive, single-file flashcard app, no build tools, no dependencies, just open `index.html` in a browser.

## Topics Covered

- **Hardware** — interrupts, system calls, MMU, kernel/user mode
- **Processes** — fork/exec/wait, PCB, signals, zombies, context switching
- **Scheduling** — FCFS, Round Robin, SJF, SRTF, EDF, Linux CFS
- **Memory Management** — paging, TLB, page faults, virtual memory, COW, ASLR
- **Concurrency** — threads, race conditions, mutexes, semaphores, deadlock, pthreads
- **I/O** — device types, DMA, polling, interrupt-driven I/O, buffering
- **Filesystems** — inodes, file allocation, directory structures, permissions
- **Networking** — OSI model, sockets, TCP/UDP, byte ordering, eBPF
- **Security** — protection rings, ACL, capabilities, buffer overflow, sandboxing

## Usage

Open `index.html` in any modern browser — no server required.

| Action | How |
|---|---|
| Flip card | Click card, press `Space` or `Enter`, or tap the flip button |
| Next card | Click `→`, press `Arrow Right`, or swipe left |
| Previous card | Click `←`, press `Arrow Left`, or swipe right |
| Filter by topic | Click a unit tab at the top |

## Structure

Everything lives in a single `index.html` file:

- **CSS** — custom properties for a paper/ink theme, card flip animation, responsive layout
- **Card data** — `ALL_CARDS` array, one object per card with `u` (unit), `q` (question), `a` (answer)
- **JS** — unit filtering, card navigation, flip logic, swipe and keyboard handling

## Adding Cards

Add an object to the `ALL_CARDS` array in `index.html`:

```js
{ u: 'Processes', q: 'Your question here?', a: 'Your answer here.' },
```

Valid unit IDs: `Hardware`, `Processes`, `Scheduling`, `Memory`, `Concurrency`, `IO`, `Filesystems`, `Networking`, `Security`.
