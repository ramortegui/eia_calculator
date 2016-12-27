# Calculator

Simple calculator server.

This calculator preserves the state(calculator memory).

It's based on Ch 5 of the book elixir in action.

## Install

    - clone the repo
    - cd eia_calculator
    - mix deps.get
    - iex -S mix

## Use
    c_pid = Calculator.start

    #PID<######>

    Calculator.value(c_pid)
    0

    Calculator.add(c_pid,1)
    {:add, 1}

    Calculator.value(c_pid)
    1

    c_pid2 = Calculator.start

    #PID<######>

    Calculator.value(c_pid2)
    0

    Calculator.add(c_pid2,10)
    {:add, 10}

    Calculator.value(c_pid2)
    10

    Calculator.value(c_pid)
    1
