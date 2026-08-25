# NFL Edge Lab — model review

Reviewed against the August 25, 2026 live build and the current MLB Edge Desk
interface.

## Calculation result

No calculation changes were needed.

The live no-bet run priced 33 upcoming games and all 198 available moneyline,
spread and total sides from real keyless prices. The 105-test offline suite
passed, including spread signs, NFL key numbers, tie pushes, de-vigging, market
anchoring, edge compression, confidence, injuries, weather, grading, CLV and
weekly limits.

The current board has one actionable candidate because this is still preseason:

- preseason games are intentionally priced but never wagered;
- the first regular-season slate is still outside the configured eight-day bet
  window;
- 288 future games with posted lines remain visible in the outlook instead of
  being mistaken for current bets.

That is a timing and exposure decision, not a broken model. Relaxing it would
create earlier, thinner positions, so the Lab preserves the existing rules.

## Design changes

- Rebuilt the interface around the compact dark-first MLB Edge Desk palette,
  typography, cards, KPI strip and mobile behavior.
- Preserved every existing data view, simulator, market, ledger and health panel.
- Renamed the user-facing PASS label to **AVOID**; the internal value remains
  `PASS`, so model logic and saved data are unchanged.

The original `nfl-edge` repository is untouched. This Lab is a separate upload.
