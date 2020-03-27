# Telegram_bot
Joke bot.

Clone code and create config file in .github/workflows/pythonapp.yml
-----------------------------------------------------
name: Python application

on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.6
      uses: actions/setup-python@v1
      with:
        python-version: 3.6
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt
    - name: Run joke
      run: |
        python -m joke.py
--------------------------------------------
