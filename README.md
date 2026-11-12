<img src="https://raw.githubusercontent.com/Beeds666/BackroomSuite-Releases/main/icon.png" width="96" align="right" alt="">

# Backroom Suite

Back-office tools for stores running AEPOS (AdvEntPOS). Backroom Suite is independent software and
isn't made or supported by AdvEntPOS.

## Install

1. Go to **[Releases](../../releases/latest)** and download `BackroomSuiteSetup-x.y.z.exe`.
2. Run it and tick the apps you want.
3. When it opens, connect to your store's AEPOS database (SQL Server, or PostgreSQL for Sypram cloud-hosted stores:
   see what each app can do on PostgreSQL below). You only do this once: every app uses the same connection.
4. The suite checks the database looks like AEPOS, then installs the apps you picked.

The hub keeps itself and the apps up to date.

## Apps

| App | What it does | SQL Server | PostgreSQL |
|---|---|---|---|
| Vendor File Formatter | Formats vendor product lists, invoices and open orders, and fills in item info from AEPOS | Yes | Not supported |
| Backroom Inventory | Counts, adjustments, receiving and transfers, staged and reviewed before they go into AEPOS; count from a phone | Everything | Item look-up, pull lists, scanning (PC and phone) and CSV export only. **Committing to AEPOS isn't available**, nor on-hand, transfers, undo or the reports |

On PostgreSQL, Backroom Inventory can't change AEPOS yet: counts can be made and exported, not committed.

## Extras

| Extra | What it is |
|---|---|
| AzureLabel shelf tag templates | Label templates and the AEPOS item query, for use in AzureLabel (bought separately from azurelabel.com; barcodes need its Pro license). Get them from **Extras** in the hub. |

## Before you start

- Windows 10 or 11, 64-bit.
- Each download has a `.sha256` checksum beside it; the hub and the apps check every update against it. The
  installers aren't code-signed yet, so Windows SmartScreen may warn: **More info → Run anyway**.
- Test versions: releases marked *Pre-release* are for PCs that ticked **Get test versions first** in the hub.
  Everyone else gets the release marked **Latest**.
- A login to your AEPOS database. The apps that change inventory always show you the changes before writing them.
- Back up your AEPOS database before using any tool that writes to it.
