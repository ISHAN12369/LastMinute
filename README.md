# LastMinute

### An AI-powered deadline co-pilot for planning, prioritizing, and finishing work on time.

LastMinute is a kinetic, browser-based productivity workspace that turns deadlines into a clear action plan. It combines task management, AI-assisted prioritization, calendar scheduling, analytics, and a focused execution mode in a single-file React application.

## Highlights

- **Deadline dashboard** — surfaces urgent work, progress, streaks, and AI-generated insights.
- **Drag-and-drop task board** — move work between pending, active, and completed states.
- **AI planner** — create, update, reschedule, and complete tasks through natural-language chat.
- **Smart calendar** — switch between week and month views and generate an AI-assisted schedule.
- **Productivity analytics** — review completion trends, activity heatmaps, and performance signals.
- **Focus mode** — isolates the next task, its countdown, subtasks, and completion action.
- **Voice controls** — supports speech input and optional spoken responses where the browser permits it.
- **Local-first persistence** — tasks, preferences, schedule, and chat history remain in `localStorage`.
- **Responsive interface** — optimized navigation and layouts for desktop, tablet, and mobile.
- **Accessible motion** — animations respect the operating system’s reduced-motion preference.

## Visual System

The interface uses a true-black canvas so every workspace feels connected. Each view receives one carefully chosen accent:

| View | Accent | Purpose |
| --- | --- | --- |
| Dashboard | Coral | Urgency and momentum |
| Task Board | Periwinkle | Structure and organization |
| AI Planner | Mint | Intelligence and forward motion |
| Calendar | Gold | Time and attention |
| Analytics | Orchid | Reflection and insight |

Polygonal surfaces, morphing ambient forms, oversized Inter typography, and GSAP-powered reveals create a distinctive visual language without obscuring the underlying productivity tools.

## Technology

- React 18
- Zustand
- HTM
- Tailwind CSS
- GSAP
- Browser `localStorage`
- Web Speech API
- Anthropic Messages API
- Groq Chat Completions API

All dependencies are loaded from CDNs, so the project requires no build step.

## Getting Started

### Quick start

Clone the repository and open `index.html` in a modern browser:

```bash
git clone https://github.com/ISHAN12369/LastMinute.git
cd LastMinute
```

For the most consistent browser behavior, serve the folder locally:

```bash
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000).

An internet connection is required on first load because the application imports its libraries and fonts from CDNs.

## AI Setup

1. Open **Settings** inside LastMinute.
2. Choose **Groq** or **Anthropic**.
3. Add your API key.
4. Save the settings.

The key is stored only in the browser’s `localStorage` and is sent directly to the selected AI provider when an AI feature is used. No API key is included in this repository.

> For a public production deployment, route provider requests through a secure backend instead of storing long-lived secrets in client-side code.

## Project Structure

```text
LastMinute/
├── index.html      # Application, state, components, and product logic
├── kinetic.css     # Scene themes, responsive styling, and kinetic visuals
└── README.md       # Project documentation
```

## Validation

The application includes a lightweight browser test overlay. Append `?test=true` to the URL to run it:

```text
http://localhost:8000/?test=true
```

The JavaScript module can also be syntax-checked with Node.js during development.

## Privacy and Security

- User data is kept locally in the browser.
- No API credentials are committed to source control.
- User input is sanitized before being included in AI prompts.
- AI requests are rate-limited client-side.
- External links use safe browser attributes where applicable.

## Browser Support

Use the latest version of Chrome, Edge, Firefox, or Safari. Voice features depend on browser support for the Web Speech API.

## Contributing

1. Create a focused feature branch.
2. Keep product behavior accessible and keyboard-friendly.
3. Respect `prefers-reduced-motion`.
4. Test desktop and mobile layouts.
5. Open a pull request describing the user impact and validation performed.

---

Built to make the last minute feel a little less last-minute.
