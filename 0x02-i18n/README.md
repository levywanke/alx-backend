# Flask i18n Project

## Overview

This project demonstrates internationalization (i18n) in a Flask web application using the Flask-Babel extension. The application supports multiple languages and time zones, allowing for localized content and user-specific settings.

## Project Structure

- `0-app.py` - Basic Flask app setup.
- `1-app.py` - Basic Babel setup with language configuration.
- `2-app.py` - Locale determination based on request headers.
- `3-app.py` - Template parameterization with translation support.
- `4-app.py` - Locale selection via URL parameters.
- `5-app.py` - Mock user login with locale and timezone settings.
- `6-app.py` - User locale preference handling.
- `7-app.py` - Time zone inference based on user settings and URL parameters.

## Dependencies

Ensure you have the following Python packages installed:

- Flask
- Flask-Babel
- pytz

You can install them using:

```bash
pip3 install Flask Flask-Babel pytz
```

## Configuration

1. **Basic Flask Setup (`0-app.py`)**

   Sets up a basic Flask app with a single route and a template displaying "Welcome to Holberton" and "Hello world".

2. **Basic Babel Setup (`1-app.py`)**

   Instantiates the Babel object, configures available languages, and sets the default locale and timezone.

3. **Get Locale from Request (`2-app.py`)**

   Implements a `get_locale` function to determine the best locale based on request headers.

4. **Parametrize Templates (`3-app.py`)**

   Uses `_()` for template localization. Configures Babel for English and French translations.

5. **Force Locale with URL Parameter (`4-app.py`)**

   Adds functionality to force a locale via URL parameters.

6. **Mock Logging In (`5-app.py`)**

   Mocks user login with predefined users and locale/timezone settings. Displays user-specific messages based on login status.

7. **Use User Locale (`6-app.py`)**

   Adjusts locale based on user preferences if available.

8. **Infer Appropriate Time Zone (`7-app.py`)**

   Determines the appropriate time zone based on URL parameters or user settings.

## Usage

1. Start the Flask application:

   ```bash
   python3 0-app.py
   ```

2. Access the application in your web browser:

   - Visit `http://127.0.0.1:5000/` to see the default content.
   - Test different locales by visiting `http://127.0.0.1:5000/?locale=[fr|en]`.
   - Test user login by visiting `http://127.0.0.1:5000/?login_as=[1|2|3|4]`.

## Translation Files

Translation files are located in the `translations` directory:

- `translations/en/LC_MESSAGES/messages.po` - English translations
- `translations/fr/LC_MESSAGES/messages.po` - French translations

To update translations, edit the `.po` files and compile them with:

```bash
pybabel compile -d translations
```

## Notes

- Ensure that all Python files have executable permissions.
- The project files must end with a newline.
- Follow `pycodestyle` for coding style compliance.
- Document all modules, classes, and functions properly.

