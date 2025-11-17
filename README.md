Windows-BAM-Analyzer is a forensic tool that reads Background Activity Moderator (BAM) artifacts from the Windows SYSTEM hive.
It identifies executed .exe files across all user SIDs and recovers possible deleted entries by scanning the raw hive.

The deleted entries feature is still a work in progress since Windows 11 doesn’t always commit or preserve deleted BAM data in the SYSTEM hive, so the results aren’t consistent :(

Features
- Extracts SYSTEM and SYSTEM.LOG1 automatically (via RawCopy)
- Reads live BAM entries from:
  HKLM\SYSTEM\CurrentControlSet\Services\bam\State\UserSettings
- Converts FILETIME values into readable timestamps
- Shows only .exe execution artifacts
- Recovers deleted/orphaned BAM entries from the raw SYSTEM hive

Usage
1. Open Command Prompt as Administrator.
2. Run the tool using the full path, for example:
   C:\BamAnalyzer\Windows-BAM-Analyzer.exe

Note
RawCopy.exe is included for convenience.
It is bundled exactly as released by the original author and used only for SYSTEM hive extraction.

Full credit to the original author:
- jschicht — RawCopy

