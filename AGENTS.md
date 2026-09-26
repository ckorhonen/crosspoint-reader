# Repository agent guide

## Repository workflow and completion

This ESP32-C3 Xteink X4 firmware uses `src/`, `include/`, `lib/`, and the `open-x4-sdk` submodule. Initialize required submodules and use PlatformIO's pinned platform/default environment. `pio run` builds; CI also runs `pio check --fail-on-defect low --fail-on-defect medium --fail-on-defect high`. `bin/clang-format-fix` rewrites files; inspect its diff.

Build invokes HTML generation, so preserve source/generated ownership. A test README alone is not a runnable suite. Flashing, partition changes, and SD writes need intended device/data authorization. Report compile/static analysis separately from physical display, controls, and storage acceptance.

Continue the authorized change through relevant validation and repair of failures it causes; preserve unrelated work. Report checks actually run, commands only inspected, and exact missing prerequisites. Ask only when a material decision, missing authorization, or required input blocks progress; continue independent reversible work. Existing mandatory contribution and validation gates still apply.
