# Heroku Buildpack for Brave Browser

This buildpack installs Brave Browser on Heroku, allowing you to run Brave Browser in a headless mode for automation tasks.

## Usage

To use this buildpack, you can either:

1. Set it as the default buildpack for your app:
```bash
heroku buildpacks:set https://github.com/yourusername/heroku-buildpack-brave-browser
```

2. Or add it to your app's buildpack list:
```bash
heroku buildpacks:add https://github.com/yourusername/heroku-buildpack-brave-browser
```

## Features

- Installs Brave Browser and all required dependencies
- Sets up a virtual display using Xvfb for headless operation
- Configures Brave Browser to run in headless mode by default
- Provides a wrapper script for easy execution

## Configuration

You can configure the following environment variables:

- `BRAVE_BROWSER_VERSION`: Specify the version of Brave Browser to install

## Example Usage

After deploying, you can use Brave Browser in your application like this:

```bash
# Run Brave Browser in headless mode
brave-browser --no-sandbox --headless

# Or use the wrapper script
brave --no-sandbox --headless
```

## Requirements

- Your application must have a `package.json` file
- The buildpack requires the following Heroku stack: `heroku-22` or newer

## License

MIT 