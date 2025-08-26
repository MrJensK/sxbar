# sxbar
The simple, yet powerful, status bar for Xorg.

#FORK

Improved Multi-Monitor Workspace Box Handling
This fork enhances sxbar so that workspace boxes on each monitor only show windows actually present on that monitor—just like dwmbar.

Changes
Per-monitor window counting:
Workspace boxes now only count windows located on the current monitor, instead of showing all windows across all screens.
New helper function:
Added window_on_monitor(Window win, int monitor_index) to determine if a window belongs to a specific monitor.
Workspace box logic update:
The workspace box drawing code now uses this function to filter windows per monitor.
Result
Each sxbar instance displays accurate workspace status for its own screen.
Workspace boxes are now more informative and reflect the actual window layout on each monitor.
