# React Router Dom Catch-All Route Conflict

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router Dom.  The `/*` route, intended to handle unmatched routes, can conflict with other routes if not placed correctly within the route hierarchy.

## Problem
The catch-all route, if placed before more specific routes, will match all paths, effectively overriding all other routes. This results in the catch-all component being rendered even when a specific route should be shown.  This example shows this scenario and its resolution.

## Solution
The solution is simple: place the catch-all route (`/*`) at the very end of your route definitions within the `<Routes>` component. This ensures that more specific routes are checked before resorting to the catch-all.