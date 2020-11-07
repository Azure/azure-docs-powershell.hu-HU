---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: bdf81228be883d57ecc282aabdf334d7410e339b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668346"
---
# <span data-ttu-id="e3ed2-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="e3ed2-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="e3ed2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ed2-103">Egy Azure Web App-bővítőhely metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="e3ed2-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="e3ed2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3ed2-104">SYNTAX</span></span>

### <span data-ttu-id="e3ed2-105">S1</span><span class="sxs-lookup"><span data-stu-id="e3ed2-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3ed2-106">S2</span><span class="sxs-lookup"><span data-stu-id="e3ed2-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3ed2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3ed2-107">DESCRIPTION</span></span>
<span data-ttu-id="e3ed2-108">A **Get-AzWebAppSlotMetric** webalkalmazás-metrikákat kap a megadott bővítőhelyhez.</span><span class="sxs-lookup"><span data-stu-id="e3ed2-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="e3ed2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e3ed2-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ed2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3ed2-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="e3ed2-111">Ez a parancs a megadott Web App percenkénti kérelmét kapja meg (PT1M-szavazási idő 1 perc) a Kezdés és a Befejezés időpontja között</span><span class="sxs-lookup"><span data-stu-id="e3ed2-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="e3ed2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3ed2-112">PARAMETERS</span></span>

### <span data-ttu-id="e3ed2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ed2-113">-DefaultProfile</span></span>
<span data-ttu-id="e3ed2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3ed2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3ed2-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="e3ed2-115">-EndTime</span></span>
<span data-ttu-id="e3ed2-116">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="e3ed2-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-117">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="e3ed2-117">-Granularity</span></span>
<span data-ttu-id="e3ed2-118">Granularitása</span><span class="sxs-lookup"><span data-stu-id="e3ed2-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="e3ed2-119">-InstanceDetails</span></span>
<span data-ttu-id="e3ed2-120">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="e3ed2-120">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-121">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="e3ed2-121">-Metrics</span></span>
<span data-ttu-id="e3ed2-122">Metrikák</span><span class="sxs-lookup"><span data-stu-id="e3ed2-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3ed2-123">-Name</span></span>
<span data-ttu-id="e3ed2-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e3ed2-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ed2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3ed2-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e3ed2-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3ed2-127">-Slot</span></span>
<span data-ttu-id="e3ed2-128">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="e3ed2-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="e3ed2-129">-StartTime</span></span>
<span data-ttu-id="e3ed2-130">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="e3ed2-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e3ed2-131">-WebApp</span></span>
<span data-ttu-id="e3ed2-132">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e3ed2-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ed2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ed2-133">CommonParameters</span></span>
<span data-ttu-id="e3ed2-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3ed2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ed2-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ed2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ed2-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ed2-136">INPUTS</span></span>

### <span data-ttu-id="e3ed2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e3ed2-137">System.String</span></span>

### <span data-ttu-id="e3ed2-138">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e3ed2-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e3ed2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ed2-139">OUTPUTS</span></span>

### <span data-ttu-id="e3ed2-140">Microsoft. Azure. Management. WebSites. models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="e3ed2-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="e3ed2-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3ed2-141">NOTES</span></span>

## <span data-ttu-id="e3ed2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3ed2-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3ed2-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="e3ed2-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="e3ed2-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3ed2-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e3ed2-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3ed2-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
