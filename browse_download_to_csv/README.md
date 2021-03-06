### Adding a "Download to CSV" button in a Browse Screen

1. Create a [Procedure](https://wiki.nubuilder.net/nubuilderforte/index.php/Procedures): Tab Builders -> Procedure -> Add

2. Code: BrowseDownloadToCSV

3. Give it a description. (E.g. Downloads data in a Browse Screen as a csv)

4. Paste the PHP code from the file [BrowseDownloadToCSV.php](BrowseDownloadToCSV.php) to the PHP field.

<p align="left">
  <img src="screenshots/BrowseDownloadToCSV.png">
</p>

5. Save

6. Add this JavaScript Code to your form’s *Custom Code* field:

❓ [How to add Custom Code](/common/form_add_custom_code_javascript.gif)

```
if(nuFormType() == 'browse'){
    nuAddActionButton('nuRunPHPHidden', 'Download to CSV', 'nuSetProperty("browse_sql",nuCurrentProperties().browse_sql); nuRunPHP("BrowseDownloadToCSV")');
}
```

7. Save

Now you see a new button "Download to CSV" in your Browse Screen!
