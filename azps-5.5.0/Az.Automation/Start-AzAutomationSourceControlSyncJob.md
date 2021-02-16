---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149315"
---
# <span data-ttu-id="775dc-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="775dc-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="775dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="775dc-102">SYNOPSIS</span></span>
<span data-ttu-id="775dc-103">Elindít egy Azure Automation-forrásvezérlő szinkronizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="775dc-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="775dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="775dc-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="775dc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="775dc-105">DESCRIPTION</span></span>
<span data-ttu-id="775dc-106">A Start-AzAutomationSourceControlSyncJob parancsmag elindítja az Azure Automation forrásvezérlő szinkronizálási feladatot az adott forrásvezérlő nevéhez.</span><span class="sxs-lookup"><span data-stu-id="775dc-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="775dc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="775dc-107">EXAMPLES</span></span>

### <span data-ttu-id="775dc-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="775dc-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="775dc-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="775dc-109">PARAMETERS</span></span>

### <span data-ttu-id="775dc-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="775dc-110">-AutomationAccountName</span></span>
<span data-ttu-id="775dc-111">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="775dc-111">The automation account name.</span></span>

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

### <span data-ttu-id="775dc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775dc-112">-DefaultProfile</span></span>
<span data-ttu-id="775dc-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="775dc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="775dc-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="775dc-114">-JobId</span></span>
<span data-ttu-id="775dc-115">A forrásvezérlő szinkronizálási feladatazonosítója.</span><span class="sxs-lookup"><span data-stu-id="775dc-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775dc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="775dc-116">-ResourceGroupName</span></span>
<span data-ttu-id="775dc-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="775dc-117">The resource group name.</span></span>

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

### <span data-ttu-id="775dc-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="775dc-118">-SourceControlName</span></span>
<span data-ttu-id="775dc-119">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="775dc-119">The source control name.</span></span>

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

### <span data-ttu-id="775dc-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="775dc-120">-Confirm</span></span>
<span data-ttu-id="775dc-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="775dc-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775dc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="775dc-122">-WhatIf</span></span>
<span data-ttu-id="775dc-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="775dc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="775dc-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="775dc-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775dc-125">CommonParameters</span></span>
<span data-ttu-id="775dc-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="775dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775dc-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="775dc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775dc-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="775dc-128">INPUTS</span></span>

### <span data-ttu-id="775dc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="775dc-129">System.String</span></span>

## <span data-ttu-id="775dc-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="775dc-130">OUTPUTS</span></span>

### <span data-ttu-id="775dc-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSync Automation</span><span class="sxs-lookup"><span data-stu-id="775dc-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="775dc-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="775dc-132">NOTES</span></span>

## <span data-ttu-id="775dc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="775dc-133">RELATED LINKS</span></span>
