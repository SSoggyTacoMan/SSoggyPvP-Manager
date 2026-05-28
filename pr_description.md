🎯 **What:** The testing gap addressed
The `YamlUtil.getSafeFile` method lacked error testing, specifically for cases where path traversal strings like '../config.yml' are provided.

📊 **Coverage:** What scenarios are now tested
Test cases have been added to verify that `YamlUtil.loadSection` correctly handles and blocks path traversal attempts by returning null. Similarly, `YamlUtil.saveConfig` has been tested to assure it safely rejects inputs attempting to write outside the configured data folder. Additionally, null safety for `dataFolder` and `filename` has been tested.

✨ **Result:** The improvement in test coverage
The error paths and null guarding within `YamlUtil` now have specific tests, increasing overall code reliability and testing coverage for filesystem operations.
🧪 [testing] Add unit tests for CommandUtil

🎯 **What:** Added missing unit test coverage for `CommandUtil.java`, specifically testing the `requirePlayer` method.
📊 **Coverage:** Covered both successful execution when a `Player` sender is passed and failure scenarios (returning `null` and sending color-translated error messages) when a non-Player `CommandSender` is passed.
✨ **Result:** Increased codebase reliability by ensuring the core utility method `requirePlayer` handles different implementations of Bukkit's `CommandSender` correctly as expected without regressions.
