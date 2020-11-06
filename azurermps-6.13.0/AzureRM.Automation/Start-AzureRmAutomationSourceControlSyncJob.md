---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 4a5864e9572a21442a5333232fe5f705fb1b5687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492022"
---
# <span data-ttu-id="bc277-101">Start-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="bc277-101">Start-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="bc277-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc277-102">SYNOPSIS</span></span>
<span data-ttu-id="bc277-103">Az Azure automatizálási verziókövetés szinkronizálási feladatát indítja el.</span><span class="sxs-lookup"><span data-stu-id="bc277-103">Starts an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc277-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc277-104">SYNTAX</span></span>

```
Start-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc277-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc277-105">DESCRIPTION</span></span>
<span data-ttu-id="bc277-106">A Start-AzureRmAutomationSourceControlSyncJob parancsmag az Azure automatizálási mártás-vezérlő szinkronizálási feladatát indítja el a megadott forráscím nevéhez.</span><span class="sxs-lookup"><span data-stu-id="bc277-106">The Start-AzureRmAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="bc277-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc277-107">EXAMPLES</span></span>

### <span data-ttu-id="bc277-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bc277-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="bc277-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc277-109">PARAMETERS</span></span>

### <span data-ttu-id="bc277-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc277-110">-AutomationAccountName</span></span>
<span data-ttu-id="bc277-111">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="bc277-111">The automation account name.</span></span>

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

### <span data-ttu-id="bc277-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc277-112">-DefaultProfile</span></span>
<span data-ttu-id="bc277-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc277-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc277-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="bc277-114">-JobId</span></span>
<span data-ttu-id="bc277-115">A forrás vezérlő szinkronizálási feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bc277-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="bc277-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc277-116">-ResourceGroupName</span></span>
<span data-ttu-id="bc277-117">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bc277-117">The resource group name.</span></span>

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

### <span data-ttu-id="bc277-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="bc277-118">-SourceControlName</span></span>
<span data-ttu-id="bc277-119">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="bc277-119">The source control name.</span></span>

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

### <span data-ttu-id="bc277-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc277-120">-Confirm</span></span>
<span data-ttu-id="bc277-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc277-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc277-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc277-122">-WhatIf</span></span>
<span data-ttu-id="bc277-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc277-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc277-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc277-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc277-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc277-125">CommonParameters</span></span>
<span data-ttu-id="bc277-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc277-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc277-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc277-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc277-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc277-128">INPUTS</span></span>

### <span data-ttu-id="bc277-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bc277-129">System.String</span></span>

## <span data-ttu-id="bc277-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc277-130">OUTPUTS</span></span>

### <span data-ttu-id="bc277-131">Microsoft. Azure. Command. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="bc277-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="bc277-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc277-132">NOTES</span></span>

## <span data-ttu-id="bc277-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc277-133">RELATED LINKS</span></span>
