Reproducing problem with a "replacing" update
=======================

## Current behavior

Renovate is failing to create an update that needs to be done.

https://developer.mend.io/github/nielsbasjes/BugreportRenovateReplaceUpdate/-/job/0194df91-fbc9-73cd-b4c7-2a909cf08608

```
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=false (branch="renovate/slf4j.version")
DEBUG: Unknown value (branch="renovate/slf4j.version")
{
"content": "[content]"
"nodeName": "groupId"
"oldValue": "org.slf4j"
"newValue": "org.slf4j"
}

DEBUG: Unknown value (branch="renovate/slf4j.version")
{
"content": "[content]"
"nodeName": "artifactId"
"oldValue": "slf4j-log4j12"
"newValue": "slf4j-reload4j"
}
```
...

```
DEBUG: branches info extended
{
  "branchesInformation": [
    {
      "branchName": "renovate/slf4j.version",
      "prNo": null,
      "prTitle": "chore(deps): replace dependency org.slf4j:slf4j-log4j12 with org.slf4j:slf4j-reload4j 2.0.16",
      "result": "no-work",
      "upgrades": [
        {
          "datasource": "maven",
          "depName": "org.slf4j:slf4j-log4j12",
          "displayPending": "",
          "fixedVersion": "2.0.16",
          "currentVersion": "2.0.16",
          "currentValue": "2.0.16",
          "newValue": "2.0.16",
          "packageFile": "pom.xml",
          "updateType": "replacement",
          "packageName": "org.slf4j:slf4j-log4j12"
        }
      ]
    }
  ]
}
```

Note the `"result": "no-work",`

## Expected behavior

A proposed update is created for this change.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/34027