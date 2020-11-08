---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024911"
---
# <span data-ttu-id="72930-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="72930-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="72930-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72930-102">SYNOPSIS</span></span>
<span data-ttu-id="72930-103">Az Azure automatizálási verziókövetés szinkronizálási feladatát indítja el.</span><span class="sxs-lookup"><span data-stu-id="72930-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="72930-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72930-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72930-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72930-105">DESCRIPTION</span></span>
<span data-ttu-id="72930-106">Az Start-AzAutomationSourceControlSyncJob parancsmag egy Azure automatizálási verziókövetés szinkronizálási feladatát indítja el a megadott verziókövetés nevéhez.</span><span class="sxs-lookup"><span data-stu-id="72930-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="72930-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72930-107">EXAMPLES</span></span>

### <span data-ttu-id="72930-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="72930-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="72930-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72930-109">PARAMETERS</span></span>

### <span data-ttu-id="72930-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72930-110">-AutomationAccountName</span></span>
<span data-ttu-id="72930-111">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="72930-111">The automation account name.</span></span>

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

### <span data-ttu-id="72930-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72930-112">-DefaultProfile</span></span>
<span data-ttu-id="72930-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72930-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72930-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="72930-114">-JobId</span></span>
<span data-ttu-id="72930-115">A forrás vezérlő szinkronizálási feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="72930-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="72930-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72930-116">-ResourceGroupName</span></span>
<span data-ttu-id="72930-117">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="72930-117">The resource group name.</span></span>

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

### <span data-ttu-id="72930-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="72930-118">-SourceControlName</span></span>
<span data-ttu-id="72930-119">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="72930-119">The source control name.</span></span>

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

### <span data-ttu-id="72930-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72930-120">-Confirm</span></span>
<span data-ttu-id="72930-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72930-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72930-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72930-122">-WhatIf</span></span>
<span data-ttu-id="72930-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72930-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72930-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72930-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72930-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72930-125">CommonParameters</span></span>
<span data-ttu-id="72930-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72930-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72930-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72930-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72930-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72930-128">INPUTS</span></span>

### <span data-ttu-id="72930-129">System. String</span><span class="sxs-lookup"><span data-stu-id="72930-129">System.String</span></span>

## <span data-ttu-id="72930-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72930-130">OUTPUTS</span></span>

### <span data-ttu-id="72930-131">Microsoft. Azure. Command. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="72930-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="72930-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72930-132">NOTES</span></span>

## <span data-ttu-id="72930-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72930-133">RELATED LINKS</span></span>
