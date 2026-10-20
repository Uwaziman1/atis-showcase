# Conceptual architecture

```mermaid
flowchart TD
    Terminal["Local MetaTrader 5 terminal"] --> Inputs["Completed-bar inputs"]
    Terminal --> Telemetry["Live display telemetry"]
    Inputs --> Engine["Observation state engine"]
    Engine --> HUD["Desktop HUD"]
    Telemetry --> HUD
    Engine --> Store["Local observation history"]
    Journal["Operator journal"] --> Store
    Store --> Reports["Session and daily reports"]
```

Python and Tkinter provide the local interface; SQLite stores reporting records.
H4 supplies context and M15 supplies observation structure. Live display values
remain distinguishable from completed-bar classifications. Operator journal input
does not become a measured software observation. Email is an optional, separately
configured delivery path and is not exercised by the offline verification.

This diagram intentionally omits proprietary rules and implementation details.
