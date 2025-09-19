# DynamicDifficultyScaler

Time-agnostic Dynamic Difficulty Scaler (DDS) that scales milestone/flag value and time rewards based on player progress vs. intended visible-time pacing. The countdown timer is tracked by the game engine; DDS is given the current values when needed.

Key goals:
- Prevent reaching TARGET_POINTS too early (default target_win_time=400m).
- Reward visible time on milestones, with caps based on absolute minutes left.
- Be robust to time being added/removed so visible_elapsed never goes negative.
