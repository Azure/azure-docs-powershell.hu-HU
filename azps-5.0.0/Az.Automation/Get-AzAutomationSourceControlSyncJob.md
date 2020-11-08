---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187853"
---
# <span data-ttu-id="ffe13-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ffe13-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="ffe13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffe13-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe13-103">Az Azure automatizálási verziókövetés szinkronizálási feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ffe13-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="ffe13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffe13-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffe13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffe13-105">DESCRIPTION</span></span>
<span data-ttu-id="ffe13-106">A Get-AzAutomationSourceControlSyncJob parancsmag az Azure automatizálási verziókövetés szinkronizálási feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ffe13-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="ffe13-107">Ha egy konkrét verziókövetés-szinkronizálási feladatot szeretne beszerezni, adja meg az azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="ffe13-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="ffe13-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ffe13-108">EXAMPLES</span></span>

### <span data-ttu-id="ffe13-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ffe13-109">Example 1</span></span>
<span data-ttu-id="ffe13-110">Ez a parancs a verziókövetés VSTSNative minden automatizálási adatforrás-szinkronizálási feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="ffe13-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="ffe13-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="ffe13-111">Example 2</span></span>
<span data-ttu-id="ffe13-112">Ez a parancs a verziókövetés szinkronizálási feladatát kapja a 08d6d266-27b6-463c-beea-bc48a67ace15 VSTSNative-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="ffe13-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="ffe13-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="ffe13-113">Example 3</span></span>

<span data-ttu-id="ffe13-114">Az Azure automatizálási verziókövetés szinkronizálási feladatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ffe13-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="ffe13-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="ffe13-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="ffe13-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffe13-116">PARAMETERS</span></span>

### <span data-ttu-id="ffe13-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ffe13-117">-AutomationAccountName</span></span>
<span data-ttu-id="ffe13-118">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ffe13-118">The automation account name.</span></span>

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

### <span data-ttu-id="ffe13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe13-119">-DefaultProfile</span></span>
<span data-ttu-id="ffe13-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffe13-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffe13-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="ffe13-121">-JobId</span></span>
<span data-ttu-id="ffe13-122">A forrás vezérlő szinkronizálási feladat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ffe13-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="ffe13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe13-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffe13-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ffe13-124">The resource group name.</span></span>

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

### <span data-ttu-id="ffe13-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="ffe13-125">-SourceControlName</span></span>
<span data-ttu-id="ffe13-126">A feladat forrás-vezérlőelemének neve.</span><span class="sxs-lookup"><span data-stu-id="ffe13-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="ffe13-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe13-127">CommonParameters</span></span>
<span data-ttu-id="ffe13-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffe13-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe13-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe13-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe13-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe13-130">INPUTS</span></span>

### <span data-ttu-id="ffe13-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ffe13-131">System.String</span></span>

### <span data-ttu-id="ffe13-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ffe13-132">System.Guid</span></span>

## <span data-ttu-id="ffe13-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe13-133">OUTPUTS</span></span>

### <span data-ttu-id="ffe13-134">Microsoft. Azure. Command. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ffe13-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="ffe13-135">Microsoft. Azure. Command. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="ffe13-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="ffe13-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffe13-136">NOTES</span></span>

## <span data-ttu-id="ffe13-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffe13-137">RELATED LINKS</span></span>