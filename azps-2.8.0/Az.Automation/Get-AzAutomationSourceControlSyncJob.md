---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 8fa14eef62ac0e8a296349ff3a47cd67086bc3ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667822"
---
# <span data-ttu-id="025d5-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="025d5-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="025d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="025d5-102">SYNOPSIS</span></span>
<span data-ttu-id="025d5-103">Az Azure automatizálási verziókövetés szinkronizálási feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="025d5-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="025d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="025d5-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="025d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="025d5-105">DESCRIPTION</span></span>
<span data-ttu-id="025d5-106">A Get-AzAutomationSourceControlSyncJob parancsmag az Azure automatizálási verziókövetés szinkronizálási feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="025d5-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="025d5-107">Ha egy konkrét verziókövetés-szinkronizálási feladatot szeretne beszerezni, adja meg az azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="025d5-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="025d5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="025d5-108">EXAMPLES</span></span>

### <span data-ttu-id="025d5-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="025d5-109">Example 1</span></span>
<span data-ttu-id="025d5-110">Ez a parancs a verziókövetés VSTSNative minden automatizálási adatforrás-szinkronizálási feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="025d5-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="025d5-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="025d5-111">Example 2</span></span>
<span data-ttu-id="025d5-112">Ez a parancs a verziókövetés szinkronizálási feladatát kapja a 08d6d266-27b6-463c-beea-bc48a67ace15 VSTSNative-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="025d5-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="025d5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="025d5-113">PARAMETERS</span></span>

### <span data-ttu-id="025d5-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="025d5-114">-AutomationAccountName</span></span>
<span data-ttu-id="025d5-115">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="025d5-115">The automation account name.</span></span>

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

### <span data-ttu-id="025d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025d5-116">-DefaultProfile</span></span>
<span data-ttu-id="025d5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="025d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025d5-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="025d5-118">-JobId</span></span>
<span data-ttu-id="025d5-119">A forrás vezérlő szinkronizálási feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="025d5-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="025d5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025d5-120">-ResourceGroupName</span></span>
<span data-ttu-id="025d5-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="025d5-121">The resource group name.</span></span>

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

### <span data-ttu-id="025d5-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="025d5-122">-SourceControlName</span></span>
<span data-ttu-id="025d5-123">A feladat forrás-vezérlőelemének neve.</span><span class="sxs-lookup"><span data-stu-id="025d5-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="025d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025d5-124">CommonParameters</span></span>
<span data-ttu-id="025d5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="025d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025d5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025d5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="025d5-127">INPUTS</span></span>

### <span data-ttu-id="025d5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="025d5-128">System.String</span></span>

### <span data-ttu-id="025d5-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="025d5-129">System.Guid</span></span>

## <span data-ttu-id="025d5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="025d5-130">OUTPUTS</span></span>

### <span data-ttu-id="025d5-131">Microsoft. Azure. Command. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="025d5-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="025d5-132">Microsoft. Azure. Command. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="025d5-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="025d5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="025d5-133">NOTES</span></span>

## <span data-ttu-id="025d5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="025d5-134">RELATED LINKS</span></span>
