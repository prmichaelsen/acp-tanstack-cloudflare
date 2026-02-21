# ACP Package: tanstack-cloudflare

TanStack + Cloudflare patterns and utilities for ACP projects

## Installation

```bash
@acp.package-install https://github.com/prmichaelsen/acp-tanstack-cloudflare.git
```

Or using the installation script:

```bash
./agent/scripts/acp.package-install.sh https://github.com/prmichaelsen/acp-tanstack-cloudflare.git
```

## What's Included

<!-- ACP_AUTO_UPDATE_START:CONTENTS -->
### Commands

(No commands yet - use @acp.command-create to add commands)

### Patterns

(No patterns yet - use @acp.pattern-create to add patterns)

### Designs

(No designs yet - use @acp.design-create to add designs)
<!-- ACP_AUTO_UPDATE_END:CONTENTS -->

## Why Use This Package

(Add benefits and use cases here)

## Usage

(Add usage examples here)

## Development

### Setup

1. Clone this repository
2. Make changes
3. Run `@acp.package-validate` to validate
4. Run `@acp.package-publish` to publish

### Adding New Content

- Use `@acp.pattern-create` to create patterns
- Use `@acp.command-create` to create commands
- Use `@acp.design-create` to create designs

These commands automatically:
- Add namespace prefix to filenames
- Update package.yaml contents section
- Update this README.md

### Testing

Run `@acp.package-validate` to validate your package locally.

### Publishing

Run `@acp.package-publish` to publish updates. This will:
- Validate the package
- Detect version bump from commits
- Update CHANGELOG.md
- Create git tag
- Push to remote
- Test installation

## Namespace Convention

All files in this package use the `tanstack-cloudflare` namespace:
- Commands: `tanstack-cloudflare.command-name.md`
- Patterns: `tanstack-cloudflare.pattern-name.md`
- Designs: `tanstack-cloudflare.design-name.md`

## Dependencies

(List any required packages or project dependencies here)

## Contributing

Contributions are welcome! Please:

1. Follow the existing pattern structure
2. Use entity creation commands (@acp.pattern-create, etc.)
3. Run @acp.package-validate before committing
4. Document your changes in CHANGELOG.md
5. Test installation before submitting

## License

MIT

## Author

Patrick Michaelsen
