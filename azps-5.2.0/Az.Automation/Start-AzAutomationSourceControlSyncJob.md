---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325664"
---
# <span data-ttu-id="a2f9f-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="a2f9f-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="a2f9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f9f-103">Elindít egy Azure Automation-forrásvezérlő szinkronizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="a2f9f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2f9f-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2f9f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2f9f-105">DESCRIPTION</span></span>
<span data-ttu-id="a2f9f-106">A Start-AzAutomationSourceControlSyncJob parancsmag elindítja az Azure Automation forrásvezérlő szinkronizálási feladatot az adott forrásvezérlő nevéhez.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="a2f9f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2f9f-107">EXAMPLES</span></span>

### <span data-ttu-id="a2f9f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2f9f-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="a2f9f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2f9f-109">PARAMETERS</span></span>

### <span data-ttu-id="a2f9f-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a2f9f-110">-AutomationAccountName</span></span>
<span data-ttu-id="a2f9f-111">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-111">The automation account name.</span></span>

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

### <span data-ttu-id="a2f9f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f9f-112">-DefaultProfile</span></span>
<span data-ttu-id="a2f9f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2f9f-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="a2f9f-114">-JobId</span></span>
<span data-ttu-id="a2f9f-115">A forrásvezérlő szinkronizálási feladatazonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="a2f9f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f9f-116">-ResourceGroupName</span></span>
<span data-ttu-id="a2f9f-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-117">The resource group name.</span></span>

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

### <span data-ttu-id="a2f9f-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="a2f9f-118">-SourceControlName</span></span>
<span data-ttu-id="a2f9f-119">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-119">The source control name.</span></span>

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

### <span data-ttu-id="a2f9f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2f9f-120">-Confirm</span></span>
<span data-ttu-id="a2f9f-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2f9f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2f9f-122">-WhatIf</span></span>
<span data-ttu-id="a2f9f-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2f9f-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2f9f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f9f-125">CommonParameters</span></span>
<span data-ttu-id="a2f9f-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2f9f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f9f-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2f9f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f9f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2f9f-128">INPUTS</span></span>

### <span data-ttu-id="a2f9f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a2f9f-129">System.String</span></span>

## <span data-ttu-id="a2f9f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2f9f-130">OUTPUTS</span></span>

### <span data-ttu-id="a2f9f-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSync Automation</span><span class="sxs-lookup"><span data-stu-id="a2f9f-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="a2f9f-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2f9f-132">NOTES</span></span>

## <span data-ttu-id="a2f9f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2f9f-133">RELATED LINKS</span></span>
