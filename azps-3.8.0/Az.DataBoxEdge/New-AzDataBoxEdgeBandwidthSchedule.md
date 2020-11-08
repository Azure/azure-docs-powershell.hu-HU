---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013400"
---
# <span data-ttu-id="ebfe0-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ebfe0-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ebfe0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebfe0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfe0-103">Új sávszélesség-ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="ebfe0-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="ebfe0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebfe0-104">SYNTAX</span></span>

### <span data-ttu-id="ebfe0-105">BandwidthParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebfe0-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfe0-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfe0-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfe0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebfe0-107">DESCRIPTION</span></span>
<span data-ttu-id="ebfe0-108">A **New-AzDataBoxEdgeBandwidthSchedule** parancsmag új sávszélesség-ütemtervet hoz létre az adatmezők Edge-eszközéhez a sávszélesség-használat kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="ebfe0-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="ebfe0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ebfe0-109">EXAMPLES</span></span>

### <span data-ttu-id="ebfe0-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ebfe0-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="ebfe0-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="ebfe0-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="ebfe0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebfe0-112">PARAMETERS</span></span>

### <span data-ttu-id="ebfe0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebfe0-113">-AsJob</span></span>
<span data-ttu-id="ebfe0-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ebfe0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebfe0-115">-Sávszélesség</span><span class="sxs-lookup"><span data-stu-id="ebfe0-115">-Bandwidth</span></span>
<span data-ttu-id="ebfe0-116">Sávszélesség a Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="ebfe0-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="ebfe0-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ebfe0-117">-DaysOfWeek</span></span>
<span data-ttu-id="ebfe0-118">Ütemezett DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ebfe0-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="ebfe0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfe0-119">-DefaultProfile</span></span>
<span data-ttu-id="ebfe0-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebfe0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebfe0-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ebfe0-121">-DeviceName</span></span>
<span data-ttu-id="ebfe0-122">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="ebfe0-122">Device Name</span></span>

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

### <span data-ttu-id="ebfe0-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ebfe0-123">-Name</span></span>
<span data-ttu-id="ebfe0-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="ebfe0-124">Resource Name</span></span>

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

### <span data-ttu-id="ebfe0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfe0-125">-ResourceGroupName</span></span>
<span data-ttu-id="ebfe0-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ebfe0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ebfe0-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="ebfe0-127">-StartTime</span></span>
<span data-ttu-id="ebfe0-128">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="ebfe0-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="ebfe0-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="ebfe0-129">-StopTime</span></span>
<span data-ttu-id="ebfe0-130">Befejezési idő ütemezése</span><span class="sxs-lookup"><span data-stu-id="ebfe0-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="ebfe0-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="ebfe0-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="ebfe0-132">Korlátlan sávszélességet állít be, ha a False beállítás értéke 20 Mbps, az alapértelmezett érték lesz beállítva</span><span class="sxs-lookup"><span data-stu-id="ebfe0-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="ebfe0-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ebfe0-133">-Confirm</span></span>
<span data-ttu-id="ebfe0-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ebfe0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebfe0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfe0-135">-WhatIf</span></span>
<span data-ttu-id="ebfe0-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ebfe0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebfe0-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebfe0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebfe0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfe0-138">CommonParameters</span></span>
<span data-ttu-id="ebfe0-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebfe0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfe0-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ebfe0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfe0-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebfe0-141">INPUTS</span></span>

### <span data-ttu-id="ebfe0-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="ebfe0-142">None</span></span>

## <span data-ttu-id="ebfe0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebfe0-143">OUTPUTS</span></span>

### <span data-ttu-id="ebfe0-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ebfe0-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ebfe0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebfe0-145">NOTES</span></span>

## <span data-ttu-id="ebfe0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebfe0-146">RELATED LINKS</span></span>
