# 🐢 Turtle Race Game

A simple and fun Python game using the Turtle module where six colorful turtles race across the screen. You place a bet on a turtle color — if your turtle wins, you win!

---

## 🎮 Features

- Player places a bet on a turtle color.
- Six turtles of different colors race from left to right.
- Random speeds make each race unpredictable and exciting!
- Console displays win/lose message based on your bet.

---

## 📜 How the Code Works

```python
screen = Screen()
screen.setup(width=500, height=400)

# Initializes the screen where the race happens.

user_bet = screen.textinput(title="Make your bet", prompt="Which turtle will win the race?")

# Prompts the user to bet on a turtle by color.

colors = ["red", "orange", "yellow", "green", "blue", "purple"]
y_position = [-70, -40, -10, 20, 50, 80]


# Defines turtle colors and starting Y positions to line them up.

for turtle_index in range(0, 6):
    new_turtle = Turtle(shape="turtle")
    new_turtle.color(colors[turtle_index])
    new_turtle.penup()
    new_turtle.goto(x=-230, y=y_position[turtle_index])

# Creates each turtle, assigns its color and starting position.

while is_race_on:
    for turtle in all_turtle:
        rand_distance = random.randint(0,10)
        turtle.forward(rand_distance)

# Moves each turtle forward by a random distance, simulating a race.
if turtle.xcor() > 230:
    is_race_on = False

# Ends the race when a turtle crosses the finish line.
print(f"You've won!") or print(f"You've lost!")

---- How to Run
Clone this repo:
git clone https://github.com/yourusername/turtlerace.git

Navigate to the folder:
cd turtlerace

Run the script:
python main.py

   

