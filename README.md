<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Black+Ops+One&size=100&pause=1000&color=B700FB&center=true&width=1000&height=200&lines=RIKA-XMD" alt="Typing SVG" /></a>
> **PAIR CODE SESSION ID**

<a href='https://rika-xmd-pair.onrender.com/pair' target="_blank">
  <img alt='Pairing Code' src='https://img.shields.io/badge/Get%20Pairing%20Code-orange?style=for-the-badge&logo=opencv&logoColor=black'/>
</a>
<br> 
### GitHub Actions Workflows

#### Node.js CI

You can set up a continuous integration workflow by creating a `.github/workflows/nodejs.yml` file with the following content:

```yaml
name: Node.js CI

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:

    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]

    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}

    - name: Install dependencies
      run: npm install

    - name: Start application
      run: npm start
