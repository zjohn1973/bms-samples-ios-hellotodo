name: Website Build

on:
  schedule:
    - cron: '0 8 * * 4' # Every Thursday at 08:00
    - cron: '0 8 * * 5' # Every Friday at 08:00
    - cron: '0 8 * * 6' # Every Saturday at 08:00

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '14'

    - name: Install dependencies
      run: npm install

    - name: Build the website
      run: npm run build

    - name: Deploy
      run: npm run deploy