---
name: Bug Report
about: Report a bug to help us improve
title: '[BUG] '
labels: bug
assignees: ''
---

## Bug Description

A clear and concise description of what the bug is.

## Steps to Reproduce

1. Configure the SDK with '...'
2. Call method '...'
3. Pass parameters '...'
4. See error

## Expected Behavior

A clear and concise description of what you expected to happen.

## Actual Behavior

What actually happened instead.

## Code Example

```php
use Dimer\ForgeSDK\Configuration;
use Dimer\ForgeSDK\Api\ServersApi;

$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-token');

$api = new ServersApi(null, $config);
// Your code that produces the bug
```

## Error Output

```
Paste the full error message or stack trace here
```

## Environment

- PHP Version: [e.g., 8.1, 8.2, 8.3]
- SDK Version: [e.g., 1.0.0]
- Guzzle Version: [e.g., 7.8]
- Operating System: [e.g., Ubuntu 22.04, macOS 14]

## Additional Context

Add any other context about the problem here (screenshots, logs, etc.).

## Possible Solution

If you have any ideas on how to fix this bug, please describe them here.