---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e15e6ee6186dc19f9f85264548c1b735ea242b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844089"
---
# <span data-ttu-id="a3990-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a3990-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a3990-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3990-102">SYNOPSIS</span></span>
<span data-ttu-id="a3990-103">Új sávszélesség-ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3990-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="a3990-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3990-104">SYNTAX</span></span>

### <span data-ttu-id="a3990-105">BandwidthParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3990-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3990-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3990-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3990-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3990-107">DESCRIPTION</span></span>
<span data-ttu-id="a3990-108">A **New-AzDataBoxEdgeBandwidthSchedule** parancsmag új sávszélesség-ütemtervet hoz létre az adatmezők Edge-eszközéhez a sávszélesség-használat kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="a3990-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="a3990-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a3990-109">EXAMPLES</span></span>

### <span data-ttu-id="a3990-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a3990-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="a3990-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3990-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="a3990-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3990-112">PARAMETERS</span></span>

### <span data-ttu-id="a3990-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3990-113">-AsJob</span></span>
<span data-ttu-id="a3990-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a3990-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-115">-Sávszélesség</span><span class="sxs-lookup"><span data-stu-id="a3990-115">-Bandwidth</span></span>
<span data-ttu-id="a3990-116">Sávszélesség a Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="a3990-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a3990-117">-DaysOfWeek</span></span>
<span data-ttu-id="a3990-118">Ütemezett DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a3990-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3990-119">-DefaultProfile</span></span>
<span data-ttu-id="a3990-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3990-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3990-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a3990-121">-DeviceName</span></span>
<span data-ttu-id="a3990-122">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a3990-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3990-123">-Name</span></span>
<span data-ttu-id="a3990-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a3990-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3990-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3990-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a3990-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a3990-127">-StartTime</span></span>
<span data-ttu-id="a3990-128">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="a3990-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a3990-129">-StopTime</span></span>
<span data-ttu-id="a3990-130">Befejezési idő ütemezése</span><span class="sxs-lookup"><span data-stu-id="a3990-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="a3990-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a3990-132">Korlátlan sávszélességet állít be, ha a False beállítás értéke 20 Mbps, az alapértelmezett érték lesz beállítva</span><span class="sxs-lookup"><span data-stu-id="a3990-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3990-133">-Confirm</span></span>
<span data-ttu-id="a3990-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3990-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3990-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3990-135">-WhatIf</span></span>
<span data-ttu-id="a3990-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3990-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3990-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3990-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3990-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3990-138">CommonParameters</span></span>
<span data-ttu-id="a3990-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3990-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3990-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3990-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3990-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3990-141">INPUTS</span></span>

### <span data-ttu-id="a3990-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="a3990-142">None</span></span>

## <span data-ttu-id="a3990-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3990-143">OUTPUTS</span></span>

### <span data-ttu-id="a3990-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a3990-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a3990-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3990-145">NOTES</span></span>

## <span data-ttu-id="a3990-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3990-146">RELATED LINKS</span></span>
