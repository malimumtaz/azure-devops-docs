---
title: Checkout (or Edit) command
titleSuffix: Azure Repos
description: Checkout (or Edit) command
ms.assetid: 377fec8a-bdc5-4e3c-ac8c-79ee85eef4ce
ms.technology: devops-code-tfvc
ms.topic: reference
ms.date: 06/30/2022
monikerRange: '<= azure-devops'
---


# Checkout (or Edit) command

[!INCLUDE [version-lt-eq-azure-devops](../../includes/version-lt-eq-azure-devops.md)]
[!INCLUDE [version-vs-gt-2013](../../includes/version-vs-gt-2013.md)]

Checks out a file and changes its pending change status to Edit. You can call this command using either **Checkout** or **Edit**.

## Prerequisites

See  [Default TFVC permissions](../../organizations/security/default-tfvc-permissions.md).

## Syntax

```
tf checkout [/lock:(none|checkin|checkout)] [/recursive] [/encoding:encoding] itemspec [/login: username,[password]]
```

## Parameters

|**Parameter**|**Description**|
|---|---|
|**/encoding**|Ignore this parameter.|
|*itemspec*|Specifies the scope of the items to check out. For syntax, see [Use Team Foundation version control commands](use-team-foundation-version-control-commands.md).|
|**/lock**|Applies or removes a lock. See [Use Team Foundation version control commands](use-team-foundation-version-control-commands.md#itemspec).|
|**/login**:*username*,[*password*]|Specifies the user account to run the command. See [Use Team Foundation version control commands](use-team-foundation-version-control-commands.md).|
|**/recursive**|Recursively checks out items in the specified directory and any subdirectories.|

## Examples

### Check out a single item

```
c:\code\SiteApp\Main\SolutionA\Project1\>tf checkout program.cs
```

Checks out program.cs.

### Check out two items

```
c:\code\SiteApp\Main\SolutionA\Project1\>tf checkout program1.cs program2.cs
```

Checks out the files program1.cs and program2.cs.

## Work in Visual Studio

-    [Check out and edit files](check-out-edit-files.md)  Use Visual Studio to check out files.

## Tips

-   ![Tip](media/checkout-or-edit-command/IC572374.png) If you are beginning a new task, it's probably a good idea for you to download the latest files from the server before you check out files and begin your work. See [Get command](get-command.md).

-   ![Tip](media/checkout-or-edit-command/IC572374.png) When you begin editing a file in a [local workspace](decide-between-using-local-server-workspace.md), it is automatically checked out for you.

-   ![Tip](media/checkout-or-edit-command/IC572374.png) You can view a list of your pending changes:

    -   And work with related data such as Comments and Associated Work Items in the **Check In** dialog box using the [Checkin command](checkin-command.md).

    -   At the command prompt by using the [Status command](status-command.md).

-   ![Tip](media/checkout-or-edit-command/IC572374.png) When you are ready to check in your changes to the team's codebase on the server, use the [Checkin command](checkin-command.md).

-   ![Tip](media/checkout-or-edit-command/IC572374.png) If you need to set aside changes (and perhaps also want to clean your workspace for another task), use the [Shelve Command](shelve-command.md).

-   ![Tip](media/checkout-or-edit-command/IC572374.png) If you use a [server workspace](decide-between-using-local-server-workspace.md), files that you have not checked out are read-only.
