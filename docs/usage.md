# How to Use WinFindGrep

This guide will walk you through the steps to effectively use WinFindGrep for your searching and replacing needs.

## Getting Started: The Main Interface

WinFindGrep provides a straightforward graphical user interface (GUI) to manage your searches. Here's an overview of the main components and how to use them:

1.  **"Find what:" Field:**
    *   Enter the text, phrase, or pattern you want to search for in your files.

2.  **"Replace with:" Field (Optional):**
    *   If you intend to replace the found text, enter the replacement text here. If you only want to find text, leave this field empty.

3.  **"File filter(s):" Field:**
    *   Specify the types of files you want to search within. 
    *   You can enter multiple filters separated by commas (e.g., `*.txt, *.log, *.cs`).
    *   The default filter is `*.txt`.

4.  **"Directory(ies):" Field:**
    *   Enter the full path to the directory (or directories) where WinFindGrep should perform the search.
    *   To search in multiple directories, separate each path with a comma.
    *   You can also use the "Browse..." button next to this field to select directories using a folder dialog.

5.  **Search Options (Checkboxes):**
    *   **Match whole word only:** If checked, WinFindGrep will only find occurrences where the search term appears as a whole word (not as part of a larger word).
    *   **Match case:** If checked, the search will be case-sensitive (e.g., "Text" will not match "text").
    *   **In all sub-folders:** If checked, WinFindGrep will recursively search through all subdirectories within the specified directory(ies).
    *   **In hidden folders:** If checked, the search will include hidden folders and files.

6.  **Search Mode (Radio Buttons):**
    *   **Normal:** Performs a standard, literal text search.
    *   **Extended (\n, \r, \t, \\, \0):** Allows you to use escape sequences in your "Find what:" field. For example:
        *   `\n` for newline
        *   `\r` for carriage return
        *   `\t` for tab
        *   `\\` for a literal backslash
        *   `\0` for a null character
    *   **Regular expression:** Enables you to use powerful regular expressions for complex pattern matching in your "Find what:" field.

7.  **Action Buttons:**
    *   **Find All:** Click this button to start the search operation based on your entered criteria. Results will be displayed in the area below.
    *   **Replace in Files:** After performing a search and specifying replacement text, click this button to replace all found occurrences in the relevant files. *Use with caution, as this will modify your files.* Consider backing up important files before using this feature extensively.
    *   **Stop:** This button becomes active during a search or replace operation and allows you to halt the process.

## Understanding the Results

When you perform a "Find All" operation, the results are displayed in a list. Each entry typically shows:

*   **File Path:** The full path to the file where the text was found.
*   **Line Number:** The line number where the match occurred.
*   **Line Content:** The actual content of the line containing the match.

**Tip:** You can usually double-click a result in the list to open the file directly in your default text editor, often navigating to the specific line.

## Examples

Here are a few examples to illustrate how you can use WinFindGrep for common tasks:

### Example 1: Finding a Specific Function Name in Code Files

Imagine you're a developer and want to find all occurrences of a function named `CalculateTotal` in your C# project files.

*   **Find what:** `CalculateTotal`
*   **Replace with:** (Leave empty)
*   **File filter(s):** `*.cs`
*   **Directory(ies):** `C:\Projects\MySolution\` (or your project's path)
*   **Search Options:** 
    *   Check "Match whole word only" (to avoid matching `CalculateTotalAmount`).
    *   Check "In all sub-folders".
*   **Search Mode:** `Normal`
*   **Action:** Click "Find All"

### Example 2: Searching for an Error Message in Log Files (Case Insensitive)

You need to find all instances of "database connection error", regardless of casing, in your application's log files from the past week.

*   **Find what:** `database connection error`
*   **Replace with:** (Leave empty)
*   **File filter(s):** `*.log`
*   **Directory(ies):** `C:\AppLogs\` (or wherever your logs are stored)
*   **Search Options:**
    *   Uncheck "Match case".
    *   Check "In all sub-folders".
*   **Search Mode:** `Normal`
*   **Action:** Click "Find All"

### Example 3: Finding All TODO Comments using Regular Expressions

You want to find all lines containing "TODO:" or "todo:" followed by any text in any file type within a specific project.

*   **Find what:** `(?i)TODO:.*`  (The `(?i)` makes the regex case-insensitive for "TODO:", `.*` matches any characters after it)
*   **Replace with:** (Leave empty)
*   **File filter(s):** `*.*` (to search all files)
*   **Directory(ies):** `D:\Work\ProjectX\`
*   **Search Options:**
    *   Check "In all sub-folders".
*   **Search Mode:** `Regular expression`
*   **Action:** Click "Find All"

### Example 4: Searching for Lines Containing Specific Tab-Separated Values (Extended Mode)

You have a set of `.tsv` (tab-separated values) files and you're looking for lines that contain "ProductA" followed by a tab, then "Shipped".

*   **Find what:** `ProductA\tShipped`
*   **Replace with:** (Leave empty)
*   **File filter(s):** `*.tsv`
*   **Directory(ies):** `C:\Data\Reports\`
*   **Search Options:**
    *   Check "In all sub-folders".
*   **Search Mode:** `Extended (\n, \r, \t, \\, \0)`
*   **Action:** Click "Find All"

These are just a few examples. Experiment with the different options and modes to tailor WinFindGrep to your specific searching needs!
