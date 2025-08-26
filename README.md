# sxbar
The simple, yet powerful, status bar for Xorg.

#FORK

## Improved Multi-Monitor Workspace Box Handling

This patch enhances **sxbar** so that workspace boxes on each monitor and only show windows actually present on that monitor — like dwmbar.

### Changes
- **Added visual workspace window boxes (max 4)** 

- **Per-monitor window counting:**  
  Workspace boxes now only count windows located on the current monitor, instead of showing all windows across all screens.
- **New helper function:**  
  Added `window_on_monitor(Window win, int monitor_index)` to determine if a window belongs to a specific monitor.
- **Workspace box logic update:**  
  The workspace box drawing code now uses this function to filter windows per monitor.

### Result

- Each sxbar instance displays accurate workspace status for its own screen.
- Workspace boxes are informative and reflect the window layout on each monitor.
