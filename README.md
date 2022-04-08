# VS Code IntelliSense Sense Bug with `os_log`

Visual Studio Code IntelliSense incorrectly reports missing `;` for the `os_log()` functions:

<img width="912" alt="Screen Shot 2022-04-08 at 18 44 15" src="https://user-images.githubusercontent.com/287778/162486480-ac91d3e4-9866-4ef8-a24f-dd510b4c19cf.png">

## Reproduction code

```cpp
#include <os/log.h>

int main() {
  // IntelliSense error: expected a ';'C/C++(65)
  os_log_info(OS_LOG_DEFAULT, "Hello world!");
  return 0;
}
```
