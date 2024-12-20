# Expo Development Server Intermittent Failure

This repository demonstrates a bug encountered with the Expo CLI where the development server intermittently fails to start, displaying an unclear WebSocket error.  The issue is sporadic and difficult to consistently reproduce.  This repository provides code examples illustrating the context in which the error occurred and the solution that resolved it.

## Bug Description
The Expo development server would occasionally fail to start during development.  The error messages were inconsistent and did not provide specific clues to the root cause.  No clear pattern could be identified for the failure.  Restarting the machine or the development server might sometimes resolve the issue, but it was not reliable.

## Solution
The problem was traced to an issue where the Metro bundler was conflicting with a previously running process using a similar port range.  The solution was to identify the conflicting process and either stop it or use a different port for the Expo development server. 

## How to Reproduce (Potentially Unreliable)
The precise steps to reproduce this bug may not be consistent, as the issue itself is intermittent. However, trying to start the Expo development server multiple times in quick succession, especially after other processes might have been recently closed, has a higher chance of reproducing this behavior.

## License
MIT