# MOBODDY update

Five-session repeating cycle. Exactly three exercises each session, three working sets of ten reps each. Lunges and single-arm cable raises: ten per side. Start with your ten-minute easy run and lighter preparation sets. Sessions generally fit around 40–60 minutes, depending on rest, setup and machine availability; do not add work merely to fill an hour.

| Session | Exercise 1 | Exercise 2 | Exercise 3 |
| --- | --- | --- | --- |
| Upper A | Flat dumbbell bench press | HD-3200 lat pulldown | HD-3000 standing cable lateral raise |
| Lower A | HD-3403 leg press | Dumbbell Romanian deadlift / physio hip hinge | Dumbbell reverse lunge |
| Upper B | HD-3300 chest press | Chest-Supported Dumbbell Row | HD-3000 standing rope triceps pushdown |
| Lower B | Weighted-ball lateral lunge | HD-3400 leg curl | HD-3403 calf raise |
| Accessories | Pictured HOIST preacher curl machine | HD-3000 standing face pull | HD-3400 leg extension |

Choose training dates and rest days yourself, then continue with the next session. This is a custom adaptation informed by the Fitness Wiki and r/Fitness, rather than an unchanged named program. The app contains the research links, a YouTube demonstration for each exercise, muscle targets, cues and official machine setup pages. YouTube URLs and titles were checked on October 12, 2026. Most demonstrations use other brands of machine; consult the official HOIST setup pages for the specific controls. The photographed machine’s exact model is unconfirmed.

Use the versions of the hinge and lunges your physio taught. The hip hinge is represented by the Romanian deadlift already in the original draft, not a newly prescribed floor deadlift. No seated overhead pressing is programmed. Stand between seated machine sets; do not progress a movement that aggravates symptoms.

## Install the update

Replace these three files at the root of your existing GitHub repository:

- `index.html`
- `sw.js`
- `manifest.json`

Keep the existing icons (identical copies are included). Publish through your existing GitHub Pages setup. Use the same website address and existing phone installation. Do not uninstall the app or clear its website data. Open it online after publishing, close/reopen it if the old version remains, and look for “5-Session Cycle” in the header. The updated service worker refreshes HTML online and keeps a cached copy for offline use. Videos and external setup pages require internet access. Changes have not been pushed to GitHub.

## Phone data

The original `history` and `profile` localStorage keys and saved data format are retained. Existing logs remain available in Guide & backup, including exercises removed from the routine. Existing suggestions are retained for unchanged dumbbell exercises; new machine exercises have separate IDs so old dumbbell weights are not reused as machine weights.

Data lives locally in the browser/PWA storage on your phone, not in GitHub or an account. Browser and installed-PWA storage behavior can differ by device. Keep using the same installation and address. Clearing website data, uninstalling, switching browsers or changing devices can lose access. Once updated, use Guide & backup → Download backup regularly; Restore a backup replaces the local history/profile after confirmation. Unfinished set entries automatically save in a separate local progress record as you type and survive reloads. Each exercise also has a Save progress button. Log this session writes completed history and clears that session’s temporary entries. Clear inputs clears the current session’s temporary entries. Backup files contain completed history and profile; unfinished progress stays on this phone.

## Validation

Checked: JavaScript syntax; five sessions with three exercises and 3×10 targets; legacy storage preservation; most-frequent prior-session weight suggestion; manual weight entry; failed save/retry without duplicate history; invalid and valid backup restore; service-worker installation and offline HTML fallback; prior app-cache cleanup without deleting other apps’ caches; external requests unaffected. Browser checks confirmed mobile layout, saving a session, persistence after reload, next-session suggestion and backup/history controls. Offline behavior was checked with service-worker tests, not on a physical phone.

## Workout calendar

Guide & backup now starts with a monthly calendar. Green days have at least one saved workout, using device-local dates. Browse previous/next months or return to the current month. Existing logs and restored backups populate it automatically. Update index.html and sw.js together for this addition.

## Temporary workout saving

Every exercise has Save progress with a saved-time message. Entries also save automatically as you type. Reopening restores the unfinished session and its numbers without logging it as a completed workout. Logging it completes the session and adds it to the calendar. Checked automatic save, reload recovery, blank-field recovery, finished-draft cleanup, interrupted cleanup and preserving another unfinished session.

## Simple suggested weights

Suggested is the most frequently used weight from the latest logged session of that exact exercise. Example: 20 lb × 10, 20 lb × 8, 15 lb × 10 → 20 lb. Reps do not affect the calculation. Ties use the first logged weight. First-time exercises show a dash. No automatic increases, decreases or prefilled weights; enter each weight yourself. Previously saved temporary entries still restore.

## October 12 update

All new workout weights are entered in lbs: per dumbbell, total ball weight, or the machine’s lbs marking. Legacy dumbbell numbers are interpreted as lbs and retained; legacy machine/ball numbers are interpreted as kg and converted for display using 1 kg = 2.2046226218 lb. Original historical numbers remain stored with explicit source units. New backup files include exercise units, so restoring them does not convert weights twice. Unfinished legacy drafts convert once and save with an lb unit marker.

Upper B now uses Chest-Supported Dumbbell Row (3 × 10), with a separate exercise ID so old machine-row weights are not suggested. Prior Mid Row history remains visible.

ATHLEAN-X is prioritized for matching exercise tutorials: dumbbell bench press, the supplied lat-pulldown video, Romanian deadlift, reverse lunge, triceps pushdown and face pull. Exact demonstrations from other creators remain where no matching ATHLEAN-X tutorial was found. The new row uses Human Kinetics’ two-dumbbell demonstration from the shared conversation. Machine chest press now uses PureGym’s newer demonstration. Every card names its video channel. All 15 video links and titles were checked.

Deploy index.html and sw.js together. README.md is updated documentation; manifest.json is unchanged. Before deploying, download a current phone backup and keep the same PWA installation and address.

### Readable progress export

Guide & backup → **Download progress report for AI** exports a Markdown file with the routine, completed sessions and every set in lbs, first/latest exercise comparisons, training context, and a review prompt. Upload it to your preferred LLM for feedback. Review the included tailbone context before sharing. Unfinished drafts are excluded. JSON backups remain the restore format.
