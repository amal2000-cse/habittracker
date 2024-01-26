# Habit Tracker Application

Welcome to the Habit Tracker application! This application helps you track your habits by allowing you to add new habits and mark whether they have been done or are still pending. The state management is handled using Redux Toolkit.

## Getting Started

To get started with the Habit Tracker application, make sure you have the necessary dependencies installed:

npm install

npm start

# Usage

## Adding a New Habit:

To add a new habit, dispatch the addHabit action with the habit name. The habit will be added to the list with a default weekly log.

## Deleting a Habit:

To delete a habit, dispatch the deleteHabit action with the habit ID.

dispatch(deleteHabit(habitId));

## To mark a habit as done on a specific day, dispatch the habitDone action with the habit ID and the day index (0-6 for Sunday to Saturday).

dispatch(habitDone({ habitId, dayIndex }));

## Marking a Habit as Not Done:

To mark a habit as not done on a specific day, dispatch the habitUnDone action with the habit ID and the day index.

dispatch(habitUnDone({ habitId, dayIndex }));

## Resetting Habit Status:

To reset the status of a habit for a specific day, dispatch the habitNone action with the habit ID and the day index.

dispatch(habitNone({ habitId, dayIndex }));

# Code Structure

The application uses Redux Toolkit for state management, with a single slice named habitsSlice:

habitsSlice.js: Contains the slice with reducers for adding, deleting, and updating habit status.
