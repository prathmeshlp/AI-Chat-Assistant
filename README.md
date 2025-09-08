# AI Interface Prototype

A modern, unified front-end prototype that combines the best features of popular AI tools into a single, responsive interface. Built with React, TypeScript, and Tailwind CSS.

## Live Demo

Vercel Link - https://ai-chat-assistant-brown.vercel.app/
StoryBook Link - https://ai-chat-clone-storybook.vercel.app/

## Research

This project is inspired by the strengths of leading AI interfaces:

1.  **OpenAI Playground:** OpenAI Playground: This tool is great for playing around with AI settings. I really liked how I could tweak things like temperature and top-p to make the AI's responses more creative or super precise, which is perfect for developers or anyone who wants control over the output.

2.  **Hugging Face Spaces:**  I was amazed by how many AI models are available here! It's like a huge library where anyone can share their own models, and I could easily try out new ones through their trending apps or "Spaces of the Week" section.

3.  **Anthropic Claude:** Claude has a clean, easy-to-use chat interface that I found super smooth. It’s awesome at handling long documents or conversations, which makes it great for digging deep into analysis or team projects.

4.  **Google Gemini:** This one stood out because it connects so well with Google apps like Gmail and Calendar. I could get answers or pull info without jumping between apps, which feels really practical for everyday tasks.

5.  **Perplexity AI:** I loved how Perplexity gives sources for every answer it provides. It makes the responses feel trustworthy since I can check where the info came from, which is super helpful for research or fact-checking.


## Selected Features

Based on the research, the following key features will be implemented:

-   **Parameter Control Panel:** Sliders to adjust AI settings, like in OpenAI Playground.
-   **Multi-Model Selector:** A model selector with lots of community-built options, inspired by Hugging Face Spaces.
-   **Clean Chat Interface:** A clean, user-friendly chat interface that can handle long texts, like Claude.
-   **Source Citations:** Citations for every answer to keep things transparent, like Perplexity AI.
-   **Light/Dark Theme Toggle:** A persistent theme switcher for user preference, following modern UX standards.

## Design

https://uxpilot.ai/s/37dac5aa4716d46b7804c0d5b5fa8532

The UI is designed for clarity and functionality, built using a Tailwind CSS-first approach.

### Tailwind Token Mapping

-   **Colors:**
    -   Primary: `indigo-600` (Buttons, Highlights)
    -   Background (Light): `white` & `gray-100`
    -   Background (Dark): `gray-900` & `gray-800`
    -   Text (Light): `gray-800` & `gray-600`
    -   Text (Dark): `gray-200` & `gray-400`
    -   Accent (Citations): `blue-500`
-   **Typography:**
    -   Font Family: Tailwind's `font-sans` (system UI)
    -   Headings: `font-semibold`
    -   Code/Mono: `font-mono` `text-sm`
-   **Spacing & Layout:**
    -   Global Padding: `p-4` `md:p-6`
    -   Section Margins: `space-y-4` `md:space-y-6`
    -   Input/Output Area: `p-4`

### Implementation Plan

The main interface will be a flexbox layout that transitions to a grid on larger screens.
-   The `Model Selector` will be a styled `<select>` element or a custom dropdown component.
-   The `Parameter Panel` will use `<input type="range">` elements styled with Tailwind for the sliders.
-   The `Chat Interface` will be a div container holding individual `ChatBubble` components, conditionally styled based on the sender (user/ai).
-   The `Citation` feature will be implemented as a clickable badge (`<a>` tag styled as a badge) below an AI response.

## Development

### Tech Stack

-   **Framework:** React 18 with Functional Components
-   **Language:** TypeScript (Strict Mode)
-   **Styling:** Tailwind CSS v3.4.17
-   **Component Development:** Storybook
-   **Deployment:** Vercel

### Getting Started

1.  **Clone the repository:**
    
    git clone <your-repo-url>
    cd your-ai-app


2.  **Install dependencies:**
    npm install

3.  **Run the development server:**
    npm start

4.  **Run Storybook to view components:**
    npm run storybook

### Project Structure
src/
    ├── components/ # Reusable UI components (Button, Slider, ChatBubble, etc.)
    ├── stories/ # Storybook stories for components
    ├── data/ # Mock JSON data for models and prompts
    └── App.tsx # Main application component    
