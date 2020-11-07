---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 61e63d2b3c66c17ce32d8b4c7346adba5879f7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667719"
---
# <span data-ttu-id="b09fa-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b09fa-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="b09fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b09fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b09fa-103">Az Azure automatizálási verziókövetés szinkronizálási feladatát indítja el.</span><span class="sxs-lookup"><span data-stu-id="b09fa-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="b09fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b09fa-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b09fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b09fa-105">DESCRIPTION</span></span>
<span data-ttu-id="b09fa-106">Az Start-AzAutomationSourceControlSyncJob parancsmag egy Azure automatizálási verziókövetés szinkronizálási feladatát indítja el a megadott verziókövetés nevéhez.</span><span class="sxs-lookup"><span data-stu-id="b09fa-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="b09fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b09fa-107">EXAMPLES</span></span>

### <span data-ttu-id="b09fa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b09fa-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="b09fa-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b09fa-109">PARAMETERS</span></span>

### <span data-ttu-id="b09fa-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b09fa-110">-AutomationAccountName</span></span>
<span data-ttu-id="b09fa-111">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b09fa-111">The automation account name.</span></span>

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

### <span data-ttu-id="b09fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09fa-112">-DefaultProfile</span></span>
<span data-ttu-id="b09fa-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b09fa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b09fa-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="b09fa-114">-JobId</span></span>
<span data-ttu-id="b09fa-115">A forrás vezérlő szinkronizálási feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b09fa-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="b09fa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b09fa-116">-ResourceGroupName</span></span>
<span data-ttu-id="b09fa-117">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b09fa-117">The resource group name.</span></span>

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

### <span data-ttu-id="b09fa-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="b09fa-118">-SourceControlName</span></span>
<span data-ttu-id="b09fa-119">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="b09fa-119">The source control name.</span></span>

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

### <span data-ttu-id="b09fa-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b09fa-120">-Confirm</span></span>
<span data-ttu-id="b09fa-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b09fa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b09fa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b09fa-122">-WhatIf</span></span>
<span data-ttu-id="b09fa-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b09fa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b09fa-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b09fa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b09fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09fa-125">CommonParameters</span></span>
<span data-ttu-id="b09fa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b09fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09fa-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b09fa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09fa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b09fa-128">INPUTS</span></span>

### <span data-ttu-id="b09fa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b09fa-129">System.String</span></span>

## <span data-ttu-id="b09fa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b09fa-130">OUTPUTS</span></span>

### <span data-ttu-id="b09fa-131">Microsoft. Azure. Command. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b09fa-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="b09fa-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b09fa-132">NOTES</span></span>

## <span data-ttu-id="b09fa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b09fa-133">RELATED LINKS</span></span>
