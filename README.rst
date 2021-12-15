=============
OCirri server
=============

This repository, in combination with aira_, is the server part for
OCirri, the Olive Culture Irrigation app. ``aira`` is the main part and
``aira-ocirri`` is specific configuration. For the client app, use
appconvert or similar.

.. _aira: https://github.com/openmeteo/aira

When using ``aira-ocirri``, you need to use extra settings, static
files, templates, and locale paths.

For the extra settings, in your ``settings.py``, import
``extrasettings.py`` like this, just before defining the settings
starting with ``AIRA_``::

    with open("/opt/aira-ocirri/extrasettings.py") as f:
        exec(f.read())

For the static files, templates, and locale paths, and the ``static``,
``templates`` and ``locale`` directories to the respective settings,
like this::

    STATICFILES_DIRS = ["/opt/aira-ocirri/static"]
    TEMPLATES[0]["DIRS"] = ["/opt/aira-ocirri/templates"]
    LOCALE_PATHS = ["/opt/aira-ocirri/locale"]

Meta
====

© 2020-2021 University of Ioannina

This program is free software: you can redistribute it and/or modify it
under the terms of the GNU General Public License as published by the
Free Software Foundation, either version 3 of the License, or (at your
option) any later version.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
Public License for more details.

.. image:: https://ocirri.irmasys.eu/static/img/logo_olive_culture_eu.png
