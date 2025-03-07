
# Todo List App

This is a simple Todo List application built with React, Redux, and TypeScript. The application fetches a list of todos from an API, displays them, and allows users to delete a todo by clicking on it. The state of the todos is managed using Redux.

## Project Structure

- `src/actions/`: Contains action creators for fetching and deleting todos.
- `src/components/`: Contains React components, including the main `App` component.
- `src/reducers/`: Contains Redux reducers for managing the state of todos.
- `src/index.tsx`: The entry point of the application, where the Redux store is created and the app is rendered.

## Installation

To set up the project locally, clone the repository and install the dependencies:

```bash
git clone <repository_url>
cd todo-list
npm install
```

## Usage

To start the development server and run the app, use the following command:

```bash
npm start
```

This will start the development server and open the application in your browser.

## Features

- Fetches a list of todos from an external API (`https://jsonplaceholder.typicode.com/todos`).
- Displays the todos in a list, and each todo is clickable.
- When a todo is clicked, it is removed from the list.
- The state of todos is managed using Redux.

## File Descriptions

- **src/actions/todos.ts**: Contains action creators for fetching and deleting todos. The `fetchTodos` action fetches todos from the API, and the `deleteTodo` action deletes a todo by its `id`.
- **src/actions/types.ts**: Defines the action types used in the actions.
- **src/components/App.tsx**: The main React component that displays the todo list and handles user interactions (fetching todos and deleting them).
- **src/reducers/index.ts**: Combines reducers into a single root reducer using `combineReducers`.
- **src/reducers/todos.ts**: Defines the reducer function that updates the todos state based on the actions.
- **src/index.tsx**: The entry point that sets up the Redux store and renders the React application.

## How It Works

### Redux Setup
- **Actions**: In `src/actions/todos.ts`, we define actions for fetching and deleting todos. The `fetchTodos` action makes an API request and dispatches the todos to the Redux store. The `deleteTodo` action deletes a todo based on its ID.
- **Reducers**: In `src/reducers/todos.ts`, we define a reducer that listens for actions and updates the todos state. It handles both the `fetchTodos` and `deleteTodo` actions.
- **Store**: In `src/index.tsx`, we configure the Redux store with `redux-thunk` middleware to handle asynchronous actions.

### Component
- **App Component**: In `src/components/App.tsx`, the app component manages the UI. It contains:
  - A button that, when clicked, fetches the list of todos.
  - A list of todos where each item can be clicked to delete the corresponding todo.
  - A loading state that is displayed while the todos are being fetched.

## License

This project is licensed under **Private use only**.
