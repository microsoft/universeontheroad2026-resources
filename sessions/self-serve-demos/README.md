# Self-Serve Demos

For Universe on the Road locations unable to host live demos, we've provided a self-service option so attendees can still explore the latest GitHub capabilities at their own pace.

The videos can be used in two ways:
- **Screen loop:** Play a selection of videos continuously on venue screens.
- **Interactive kiosk:** Let attendees browse topics and choose which videos to watch on a touchscreen or computer.

## Download the content

Download the [Universe on the Road self-serve video content from SharePoint](https://microsofteur.sharepoint.com/:f:/t/UniverseontheRoad/cgpXzt7ikPH9RpMUBz16pDzwEgUBGfTtHA3IkAwzwAN7eVzhkA).

The content is organized into four topic groups:

| Topic | Includes |
| --- | --- |
| **GitHub Advanced Security — Found means fixed** | Code scanning, AI Scan, Copilot Autofix, secret scanning, Dependabot, and package security. |
| **GitHub Copilot — Automations, Metrics, Code Review, Cloud Agent** | Agentic workflows, automations, usage and impact metrics, and cloud-agent scenarios. |
| **GitHub Copilot — Desktop App, CLI, SDK** | Copilot app experiences, CLI workflows, projects, computer use, and SDK demonstrations. |
| **GitHub Enterprise — Scale AI-powered development with confidence** | Enterprise-scale AI development, management, and governance. |

Videos include short product demos, narrated explainers, keynote demo clips, and quiz/Q&A segments. Some include captions. Choose the videos that best suit your audience and venue setup.

## Option 1: Play videos on a loop

1. Download the video folders from SharePoint.
2. Select the videos you want to show and add them to a playlist in your venue's media player.
3. Enable repeat/loop playback and test video, audio, and captions (where available) on the display.

**Best for:** Screens that attendees can watch without interacting with them.

## Option 2: Set up the self-service kiosk

Use the [Video Kiosk repository](https://github.com/octodemo/video-kiosk) to give attendees an interactive experience: browse video categories, select a video, and watch it full screen. It supports touch, mouse, and keyboard input and can run offline once set up.

1. Install **Node.js 24 or later**.
2. Clone the kiosk repository:

   ```bash
   git clone https://github.com/octodemo/video-kiosk.git
   cd video-kiosk
   ```

3. Download the SharePoint video folders and copy them into the kiosk's `videos/` directory. **Keep the original folder and file names.**
4. Start the kiosk:

   ```bash
   npm install
   npm start
   ```

5. On the settings page (`http://127.0.0.1:3000/`), choose **JSON file**, select `catalogs/universe-on-the-road.json`, choose a theme, and click **Launch kiosk**.
6. Confirm the videos load and play correctly before the event.

For full setup, configuration, troubleshooting, and kiosk-mode instructions, see the [Video Kiosk README](https://github.com/octodemo/video-kiosk#readme).

> **Note:** The video files are hosted in SharePoint, not in the GitHub repositories. Download them before the event and test your chosen playback option on the venue hardware.