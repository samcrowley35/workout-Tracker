# workout-Tracker
Personal project, intent is to make an app that makes it easier to track progress with

Stack/technologies to use to build the web app:
- Vur, firebase, ionic (for mobile usage)
- VS code, Is there an extension that makes a webpage visible in real time?

Pages/Views:

Home Page
- Calendar of the current month, each day has rectangles within it 
- Each Rectangle has it’s own color and represents a workout
- Current day should be highlighted for easy access
- When a day is clicked on, navigate to the Day page

Day Page
- On the top of the page, there should be a day label and an add button
- Within the body of the page, there should be a list of already completed workouts
  - Each of these should have a list of the exercises, not the notes that come with them
  - Ex: Pull Workout for the title, simple list of exercises done within, respective color coding for the rectangle containing everything
    - The workout bubble could also display a little 'R^' and 'W-' string that shows what to do next time for each exercise within it
  - Push workout(green), pull workout(yellow), leg workout(red), core workout(light blue), knee-strengthening/injury prevention(purple), run(orange)
  - The already completed workouts should be just read only, there’s no need to change them
  - When the Add button is clicked, there should be a dropdown menu that pops up with each workout type, when the type is selected, navigate to the Add Workout Page with the page being color coded to the type of workout
  - First, the user will be prompted to select either a lift or a non-lift workout
  - Second, the user will be prompted to select the specific kind of lift
  
Add Workout Page
- This page/view's purpose is to gather all user input data into a workout 'object'
- Two kinds of workouts, Lift and Non-lift
  - Lift workouts have three colors: push (green), pull (yellow), legs (red)
    - When the kind of lift workout is selected from the Add Workout page/view, navigate to it's respective Page
  - Non-Lift workouts have three colors as well: core workout(light blue), knee-strengthening/injury prevention(purple), run(orange)
    - The non-lift workout page will look pretty different from the lift one
    - Exercises won't be as structured
      - Will have to think of a different way to track them
- Finish Workout button
  - When pressed, add to the day object, which will essentially be a short list of workout objects

Add Exercise Page
- Starting point?
- Components for adding a lift exercise(note: it will be implied that the number of sets is four for each):
  - Exercise name slot with an enter button
    - Drop down menu of exercises that I've done and plan on doing shows up when clicked
    - Enter button changes the view so that the button disappears and the page/view is titled with the exercise name
    - The list of exercise names and weights should be put in the database first
    - The Workout "object" should contain a list of lifts already done as well as lifts to be done
  - Increase/Decrease weight/reps from last week icons
    - Once an exercise is selected, query for the latest time it was done and figure out what the plan was for the future the last time it was done
    - The weight to increase/decrease weight/reps from should also be displayed for transparency
  - Start rest timer
    - When clicked, a two minute timer will start with a little clock counting down the seconds
  - Notes Section
    - Simple text box where bulletpoints about the lift can be put in
  - Increase/Decrease weight/reps for next time section
    - Three options for each: increase, decrease, stay the same
  - Done 
    - Exit out of the page/view
    - Add to the workout object
