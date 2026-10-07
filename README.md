# Subnet Ping Sweeper 🛰️

A highly concurrent Network Reconnaissance utility built in Python to map active endpoints across a local `/24` IPv4 subnet. Designed to replicate the initial host-discovery phase utilized by both red-team operators and SOC analysts.

**Features:**
* Utilizes Python's `concurrent.futures.ThreadPoolExecutor` to dispatch dozens of ICMP Echo Requests simultaneously, completing a full `/24` sweep in seconds rather than minutes.
* Intelligently auto-detects the host machine's local IP addressing scheme to pre-populate the target subnet prefix.
* Implements OS-aware execution parameters, ensuring `ping` commands utilize the correct timeout flags and suppressing shell consoles from interrupting the UI (`CREATE_NO_WINDOW`).
* Features a thread-safe Tkinter graphical interface that updates discovered hosts in real-time.

*Built as Day 22 of a 30-Day Network Engineering & Security portfolio streak.*
