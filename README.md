# footballManager
Football Manager for friends

# Saturday Football Team Manager

A lightweight web app to streamline your weekly Saturday football matches:

- **Quick Attendance**: Mark who’s playing today with a simple checkbox list.
- **Balanced Teams**: Automatically splits players into two teams based on attack, midfield, and defence ratings using a greedy load-balancing algorithm.
- **Manual Adjustments**: Click player names to move them between teams on the fly.
- **Score Logging**: Record match results along with team compositions, stored locally in your browser.

## Features

- Purely HTML, CSS, and vanilla JavaScript—no backend required.
- Data persistence via `localStorage` (players roster and past results).
- Responsive two-column layout:
  - **Left**: Attendance panel and “Generate Teams” button.
  - **Right**: Teams display with total ratings and match score form.
- Easy navigation between **Team Generator**, **Manage Players**, and **Previous Results** pages via a dropdown menu.

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/football-team-manager.git
   cd football-team-manager
   ```

2. **Publish to GitHub Pages**
   - Push the three HTML files (`index.html`, `players.html`, `results.html`) to the `main` branch.
   - In your repo’s **Settings > Pages**, set the source to `main`/`(root)`.
   - Visit `https://<your-username>.github.io/football-team-manager/` to use the app.

## Usage

1. **Manage Players**
   - Navigate to **Manage Players** from the dropdown.
   - Add, edit, or delete players with their Attack/Mid/Def ratings.

2. **Generate Teams**
   - Go to **Team Generator**.
   - Check off who’s present and click **Generate Teams**.
   - Teams appear with summed ratings; click names to swap players.

3. **Log Scores**
   - Enter the final score for Team A and Team B.
   - Click **Save Result** to append it to your match history.

4. **View Past Results**
   - Select **Previous Results** to review all logged matches.

## Algorithm

- **Greedy Load-Balancing**:
  1. Sort present players by total rating (Atk + Mid + Def) descending.
  2. Iteratively assign each player to the team with the lower current sum.
  3. Results in two teams with balanced overall strength.

## Contributing

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to branch: `git push origin feature/YourFeature`.
5. Open a Pull Request.

## License

This project is released under the [MIT License](LICENSE).
