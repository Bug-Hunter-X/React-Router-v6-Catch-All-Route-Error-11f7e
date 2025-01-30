# React Router v6 Catch-All Route Error

This repository demonstrates a subtle bug in React Router v6 related to catch-all routes (`/*`).  When a catch-all route is placed after other, more specific routes, it causes an error. This is because React Router matches routes from top to bottom, and the catch-all route will always match before the other routes get a chance.

The solution involves reordering the routes in the `Routes` component to ensure that the catch-all route is always the last route listed.