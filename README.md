# Monorepo for Mobile Learning Project

This repository is a monorepo containing two projects:

- **Python Agent**: A backend project managed using [Poetry](https://python-poetry.org/).
- **React Native App**: A mobile application developed with [Expo](https://expo.dev/) for React Native.

## Python Agent

The Python agent project was created using Poetry. 

**Setup Instructions:**

1. Navigate to the `python-agent` directory.
2. Install dependencies with:
   ```bash
   poetry install
   ```
3. Run the agent (assuming your main file is located at `agent/main.py`):
   ```bash
   poetry run python agent/main.py
   ```

## React Native App

The React Native app was created using Expo.

**Setup Instructions:**

1. Navigate to the `react-native-app` directory.
2. Install dependencies:
   ```bash
   npm install
   ```
   or if you are using Yarn:
   ```bash
   yarn install
   ```
3. Start the development server:
   ```bash
   expo start
   ```

## Overview

This monorepo leverages Poetry and Expo to manage the Python backend and the React Native frontend respectively. 

Use this README as a guide for setting up and developing your mobile learning application.
