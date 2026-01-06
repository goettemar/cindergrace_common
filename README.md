# Cindergrace Common

Shared utilities for Cindergrace applications.

## Installation

```bash
pip install cindergrace-common
```

For Gradio i18n support:
```bash
pip install cindergrace-common[gradio]
```

## Features

- **Configuration**: Type-safe environment variable helpers
- **Security**: Localhost-by-default server binding, feature flags
- **Branding**: Centralized logo and CSS loading
- **i18n**: YAML-based translations

## Quick Start

```python
from cindergrace_common import (
    BaseConfig, SecurityMixin, BrandingMixin,
    env_int, env_bool
)

class Config(BaseConfig, SecurityMixin, BrandingMixin):
    APP_PREFIX = "MYAPP"
    PORT = env_int("MYAPP_PORT", 7865)

# Server binds to localhost by default
# Set MYAPP_ALLOW_REMOTE=1 for network access
server_name = Config.get_server_bind()
```

## Environment Variables

| Variable | Description |
|----------|-------------|
| `{PREFIX}_PORT` | Server port |
| `{PREFIX}_ALLOW_REMOTE` | Set to `1` for network access |
| `{PREFIX}_ENABLE_{FEATURE}` | Enable specific features |
| `CINDERGRACE_BRANDING_PATH` | Path to branding assets |

## License

MIT
