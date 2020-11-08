---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181275"
---
# <span data-ttu-id="b4167-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b4167-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b4167-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4167-102">SYNOPSIS</span></span>
<span data-ttu-id="b4167-103">Új sávszélesség-ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="b4167-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="b4167-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4167-104">SYNTAX</span></span>

### <span data-ttu-id="b4167-105">UnlimitedBandwidthParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4167-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4167-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4167-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4167-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4167-107">DESCRIPTION</span></span>
<span data-ttu-id="b4167-108">A **New-AzStackEdgeBandwidthSchedule** parancsmag új sávszélesség-ütemtervet hoz létre a halom Edge-eszközéhez a sávszélesség-használat kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="b4167-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="b4167-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b4167-109">EXAMPLES</span></span>

### <span data-ttu-id="b4167-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4167-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="b4167-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="b4167-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="b4167-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4167-112">PARAMETERS</span></span>

### <span data-ttu-id="b4167-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4167-113">-AsJob</span></span>
<span data-ttu-id="b4167-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b4167-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4167-115">-Sávszélesség</span><span class="sxs-lookup"><span data-stu-id="b4167-115">-Bandwidth</span></span>
<span data-ttu-id="b4167-116">Sávszélesség a Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="b4167-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="b4167-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b4167-117">-DaysOfWeek</span></span>
<span data-ttu-id="b4167-118">Ütemezett DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b4167-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="b4167-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4167-119">-DefaultProfile</span></span>
<span data-ttu-id="b4167-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4167-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4167-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b4167-121">-DeviceName</span></span>
<span data-ttu-id="b4167-122">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="b4167-122">Device Name</span></span>

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

### <span data-ttu-id="b4167-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4167-123">-Name</span></span>
<span data-ttu-id="b4167-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b4167-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4167-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4167-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4167-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b4167-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b4167-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="b4167-127">-StartTime</span></span>
<span data-ttu-id="b4167-128">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="b4167-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="b4167-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="b4167-129">-StopTime</span></span>
<span data-ttu-id="b4167-130">Befejezési idő ütemezése</span><span class="sxs-lookup"><span data-stu-id="b4167-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="b4167-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="b4167-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="b4167-132">Korlátlan sávszélességet ad meg</span><span class="sxs-lookup"><span data-stu-id="b4167-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4167-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4167-133">-Confirm</span></span>
<span data-ttu-id="b4167-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4167-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4167-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4167-135">-WhatIf</span></span>
<span data-ttu-id="b4167-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4167-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4167-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4167-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4167-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4167-138">CommonParameters</span></span>
<span data-ttu-id="b4167-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4167-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4167-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4167-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4167-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4167-141">INPUTS</span></span>

### <span data-ttu-id="b4167-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="b4167-142">None</span></span>

## <span data-ttu-id="b4167-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4167-143">OUTPUTS</span></span>

### <span data-ttu-id="b4167-144">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b4167-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b4167-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4167-145">NOTES</span></span>

## <span data-ttu-id="b4167-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4167-146">RELATED LINKS</span></span>
