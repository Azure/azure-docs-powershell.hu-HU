---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184588"
---
# <span data-ttu-id="a7dd8-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a7dd8-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a7dd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dd8-103">Sávszélesség-ütemezés frissítése</span><span class="sxs-lookup"><span data-stu-id="a7dd8-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="a7dd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7dd8-104">SYNTAX</span></span>

### <span data-ttu-id="a7dd8-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7dd8-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7dd8-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a7dd8-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7dd8-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7dd8-114">DESCRIPTION</span></span>
<span data-ttu-id="a7dd8-115">A **set-AzDataBoxEdgeBandwidthSchedule** parancsmag frissíti az adatmezők Edge-eszköz sávszélesség-ütemezését.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="a7dd8-116">Példák</span><span class="sxs-lookup"><span data-stu-id="a7dd8-116">EXAMPLES</span></span>

### <span data-ttu-id="a7dd8-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a7dd8-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="a7dd8-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="a7dd8-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="a7dd8-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7dd8-119">PARAMETERS</span></span>

### <span data-ttu-id="a7dd8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7dd8-120">-AsJob</span></span>
<span data-ttu-id="a7dd8-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a7dd8-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7dd8-122">-Sávszélesség</span><span class="sxs-lookup"><span data-stu-id="a7dd8-122">-Bandwidth</span></span>
<span data-ttu-id="a7dd8-123">Sávszélesség a Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="a7dd8-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a7dd8-124">-DaysOfWeek</span></span>
<span data-ttu-id="a7dd8-125">Ütemezett DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a7dd8-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dd8-126">-DefaultProfile</span></span>
<span data-ttu-id="a7dd8-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7dd8-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a7dd8-128">-DeviceName</span></span>
<span data-ttu-id="a7dd8-129">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a7dd8-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7dd8-130">-InputObject</span></span>
<span data-ttu-id="a7dd8-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7dd8-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7dd8-132">-Name</span></span>
<span data-ttu-id="a7dd8-133">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a7dd8-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7dd8-134">-ResourceGroupName</span></span>
<span data-ttu-id="a7dd8-135">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a7dd8-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7dd8-136">-ResourceId</span></span>
<span data-ttu-id="a7dd8-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7dd8-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-138">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a7dd8-138">-StartTime</span></span>
<span data-ttu-id="a7dd8-139">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="a7dd8-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a7dd8-140">-StopTime</span></span>
<span data-ttu-id="a7dd8-141">Befejezési idő ütemezése</span><span class="sxs-lookup"><span data-stu-id="a7dd8-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="a7dd8-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a7dd8-143">Korlátlan sávszélességet ad meg</span><span class="sxs-lookup"><span data-stu-id="a7dd8-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7dd8-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7dd8-144">-Confirm</span></span>
<span data-ttu-id="a7dd8-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7dd8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7dd8-146">-WhatIf</span></span>
<span data-ttu-id="a7dd8-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7dd8-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7dd8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dd8-149">CommonParameters</span></span>
<span data-ttu-id="a7dd8-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7dd8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dd8-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dd8-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7dd8-152">INPUTS</span></span>

### <span data-ttu-id="a7dd8-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="a7dd8-153">None</span></span>

## <span data-ttu-id="a7dd8-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7dd8-154">OUTPUTS</span></span>

### <span data-ttu-id="a7dd8-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a7dd8-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a7dd8-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7dd8-156">NOTES</span></span>

## <span data-ttu-id="a7dd8-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7dd8-157">RELATED LINKS</span></span>
