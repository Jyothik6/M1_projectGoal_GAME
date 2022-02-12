# M1_projectGoal_GAME
name: C/C++ CI

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
      
    - name: make all
      run:  make all -C M1_projectgoal_GAME/
