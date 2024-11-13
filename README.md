# Vokarenda: Full Calendar Component built with `shadcn/ui`

## Overview

Forked from https://github.com/deiondz/shadcn-fullcalender, and setup with vite.js for create npm package, Thanks [@Deion_Dz](https://x.com/Deion_Dz) for creating base full-calendar component

## Installation

First, add `itokun99/vokarenda` package into project

```
npm install @itokun99/vokarenda
```

## Example

Minimal implementation in `src/index.tsx`

```
import { newevents } from "@/data/events";
import { Vokarenda } from "@itokun99/vokarenda";
import React from "react";
import ReactDOM from "react-dom/client";

function App() {
  return (
    <div className="container mx-auto">
      <div className="grid grid-cols-1">
        <Vokarenda
          events={newevents}
          config={{
            addEventConfig: {
              variant: "primary", // Default variant (can be 'primary', 'secondary', etc.)
              buttonText: "Add Event", // Default button text
              formTitle: "Create a New Event", // Default form title
              formDescription: "Testing", // Default form description
              icon: undefined, // Custom icon for the button, if needed
              customForm: undefined, // Custom form component, if needed
            },
            animationConfig: {
              duration: 300, // Default animation duration in milliseconds
            },
          }}
        />
      </div>
    </div>
  );
}

ReactDOM.createRoot(document.getElementById("root")!).render(<App />);
```
