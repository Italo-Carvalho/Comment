Contributing
=============

Django Comments Dab is developed and maintained by developers in an Open Source manner.
Any support is welcome. You could help by writing documentation, pull-requests, report issues and/or translations.

Starting points
^^^^^^^^^^^^^^^^

An issue with a `good first`_ label might be a good place to start with.

You can also try to take up an issue tagged with an `upcoming release`_.

.. _`good first`: https://github.com/Radi85/Comment/issues?q=is%3Aopen+is%3Aissue+label%3A"good+first+issue"
.. _`upcoming release`: https://github.com/Radi85/Comment/milestones


PR and commit messages
^^^^^^^^^^^^^^^^^^^^^^^

**Pull Requests**

Refer to `#125`_

.. _`#125`: https://github.com/Radi85/Comment/discussions/125

In order to keep the default branch clean and up to date with the current release, all PR shall be merged with ``develop`` branch.

**Commit messages**

Use one commit per issue and try to keep the first line within 50 characters.

Need more? use the commit body.

The commit message should reference the issue number in the header (first line) like so:

feat(*#NUMBER*): YOUR COMMIT

**headers:**

- feat(*#NUMBER*) for adding new feature
- fix(*#NUMBER*) for fixing a bug
- ref(*#NUMBER*) for code refactoring and enhancement
- test(*#NUMBER*) for adding, fixing or adjusting tests
- doc(*#NUMBER*) for documentation
- chore(*#NUMBER*) Changes to the build process, new releases and work doesn't relate to any of the previous header

The issue number can be skipped if not available..

Development
^^^^^^^^^^^

To start development on this project, fork_ this repository and follow the guidelines given below.

.. _fork: https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo

.. code:: bash

    # clone the forked repository
    $ git clone YOUR_FORKED_REPO_URL

    # create a virtual environment
    $ python3 -m venv local_env
    # activate the virtual environment
    $ source local_env/bin/activate
    # install dependencies
    (local_env) $ pip install -e . -r test/example/requirements.txt

    (local_env) $ export DEBUG="True"
    # migrate the changes to database
    (local_env) $ python manage.py migrate
    # prepare initial data
    (local_env) $ python manage.py create_initial_data
    # start the development server
    (local_env) $ python manage.py runserver

Or run with docker

.. code:: bash

    $ git clone YOUR_FORKED_REPO_URL
    $ cd Comment
    $ docker-compose up


Login with:

    username: ``test``

    password: ``test``

Testing
^^^^^^^

To run tests against a particular ``python`` and ``django`` version installed inside your virtual environment, you may use:

.. code:: bash

    (local_env) $ python manage.py test --settings=test.settings.test


To run tests against all supported ``python`` and ``django`` versions, you may run:

.. code:: bash

    # install dependency
    (local_env) $ pip install tox
    # run tests
    (local_env) $ tox


Translations
^^^^^^^^^^^^

To add translations in your native language, please take a look at the `instructions for translators`_.

.. _`instructions for translators`: https://django-comment-dab.readthedocs.io/i18n.html#adding-support-for-translation
