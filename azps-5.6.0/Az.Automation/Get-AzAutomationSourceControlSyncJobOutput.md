---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 369dfd85b88b079e32e9ea65513d37c99f64b6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014149"
---
# <span data-ttu-id="a62ee-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="a62ee-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="a62ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a62ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a62ee-103">Egy Azure Automation-forrásvezérlő szinkronizálási feladat kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a62ee-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="a62ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a62ee-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a62ee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a62ee-105">DESCRIPTION</span></span>
<span data-ttu-id="a62ee-106">A **Get-AzAutomationSourceControlSync JobOutput** parancsmag az Azure Automation forrásvezérlő szinkronizálási feladat kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a62ee-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="a62ee-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a62ee-107">EXAMPLES</span></span>

### <span data-ttu-id="a62ee-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a62ee-108">Example 1</span></span>
<span data-ttu-id="a62ee-109">Ez a parancs a forrásvezérlő szinkronizálási feladat kimenetét a VSTSNative forrásvezérlő 08d6d266-27b6-463c-beea-bc48a67ace15 azonosítójával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a62ee-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="a62ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a62ee-110">PARAMETERS</span></span>

### <span data-ttu-id="a62ee-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a62ee-111">-AutomationAccountName</span></span>
<span data-ttu-id="a62ee-112">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a62ee-112">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62ee-113">-DefaultProfile</span></span>
<span data-ttu-id="a62ee-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a62ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a62ee-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="a62ee-115">-JobId</span></span>
<span data-ttu-id="a62ee-116">A forrásvezérlő szinkronizálási feladatazonosítója.</span><span class="sxs-lookup"><span data-stu-id="a62ee-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a62ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="a62ee-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a62ee-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ee-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="a62ee-119">-SourceControlName</span></span>
<span data-ttu-id="a62ee-120">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="a62ee-120">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ee-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="a62ee-121">-Stream</span></span>
<span data-ttu-id="a62ee-122">Az adatfolyam típusa.</span><span class="sxs-lookup"><span data-stu-id="a62ee-122">The stream type.</span></span>
<span data-ttu-id="a62ee-123">Alapértelmezés szerint a "Bármely" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="a62ee-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ee-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="a62ee-124">-StreamId</span></span>
<span data-ttu-id="a62ee-125">A stream azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a62ee-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62ee-126">CommonParameters</span></span>
<span data-ttu-id="a62ee-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a62ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62ee-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a62ee-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62ee-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a62ee-129">INPUTS</span></span>

### <span data-ttu-id="a62ee-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a62ee-130">System.String</span></span>

### <span data-ttu-id="a62ee-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a62ee-131">System.Guid</span></span>

### <span data-ttu-id="a62ee-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncSyncStreamType</span><span class="sxs-lookup"><span data-stu-id="a62ee-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="a62ee-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a62ee-133">OUTPUTS</span></span>

### <span data-ttu-id="a62ee-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncSyncStream</span><span class="sxs-lookup"><span data-stu-id="a62ee-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="a62ee-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncSyncStreamRecord</span><span class="sxs-lookup"><span data-stu-id="a62ee-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="a62ee-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a62ee-136">NOTES</span></span>

## <span data-ttu-id="a62ee-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a62ee-137">RELATED LINKS</span></span>
