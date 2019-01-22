# Webpack Bug Reproduction

## Problem

Some libraries depend on an exported module to have __esModule === true for understanding the export is an es module. However, module concatenation doesn't work with this behavior that it doesn't have the __esModule property. The issue is reproduced in this repo.

## How to run

For reproducing the issue:
- npm start
- open index.html in your browser
- open devtools and verify the module logged doesn't have "__esModule: true" as a property.

Expected:
- npm run start:noconcat
- open index.html in your brower
- open devtools and verify the module logged has "__esModule: true" as a property
