---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: f761a84fe994f0da68b4d3a86b513ba333b06573
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842409"
---
# <span data-ttu-id="d93d7-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d93d7-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="d93d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d93d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d93d7-103">Sávszélesség-ütemezés frissítése</span><span class="sxs-lookup"><span data-stu-id="d93d7-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="d93d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d93d7-104">SYNTAX</span></span>

### <span data-ttu-id="d93d7-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d93d7-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93d7-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d93d7-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93d7-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93d7-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93d7-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93d7-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93d7-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93d7-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="d93d7-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d93d7-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="d93d7-114">DESCRIPTION</span></span>
<span data-ttu-id="d93d7-115">A **set-AzDataBoxEdgeBandwidthSchedule** parancsmag frissíti az adatmezők Edge-eszköz sávszélesség-ütemezését.</span><span class="sxs-lookup"><span data-stu-id="d93d7-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="d93d7-116">Példák</span><span class="sxs-lookup"><span data-stu-id="d93d7-116">EXAMPLES</span></span>

### <span data-ttu-id="d93d7-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d93d7-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="d93d7-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="d93d7-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="d93d7-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d93d7-119">PARAMETERS</span></span>

### <span data-ttu-id="d93d7-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d93d7-120">-AsJob</span></span>
<span data-ttu-id="d93d7-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d93d7-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d93d7-122">-Sávszélesség</span><span class="sxs-lookup"><span data-stu-id="d93d7-122">-Bandwidth</span></span>
<span data-ttu-id="d93d7-123">Sávszélesség a Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="d93d7-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="d93d7-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="d93d7-124">-DaysOfWeek</span></span>
<span data-ttu-id="d93d7-125">Ütemezett DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="d93d7-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="d93d7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93d7-126">-DefaultProfile</span></span>
<span data-ttu-id="d93d7-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d93d7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d93d7-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d93d7-128">-DeviceName</span></span>
<span data-ttu-id="d93d7-129">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="d93d7-129">Device Name</span></span>

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

### <span data-ttu-id="d93d7-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d93d7-130">-InputObject</span></span>
<span data-ttu-id="d93d7-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d93d7-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="d93d7-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d93d7-132">-Name</span></span>
<span data-ttu-id="d93d7-133">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d93d7-133">Resource Name</span></span>

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

### <span data-ttu-id="d93d7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93d7-134">-ResourceGroupName</span></span>
<span data-ttu-id="d93d7-135">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d93d7-135">Resource Group Name</span></span>

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

### <span data-ttu-id="d93d7-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d93d7-136">-ResourceId</span></span>
<span data-ttu-id="d93d7-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d93d7-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="d93d7-138">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="d93d7-138">-StartTime</span></span>
<span data-ttu-id="d93d7-139">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="d93d7-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="d93d7-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="d93d7-140">-StopTime</span></span>
<span data-ttu-id="d93d7-141">Befejezési idő ütemezése</span><span class="sxs-lookup"><span data-stu-id="d93d7-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="d93d7-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="d93d7-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="d93d7-143">Korlátlan sávszélességet ad meg</span><span class="sxs-lookup"><span data-stu-id="d93d7-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="d93d7-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d93d7-144">-Confirm</span></span>
<span data-ttu-id="d93d7-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d93d7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d93d7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d93d7-146">-WhatIf</span></span>
<span data-ttu-id="d93d7-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d93d7-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d93d7-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d93d7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d93d7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93d7-149">CommonParameters</span></span>
<span data-ttu-id="d93d7-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d93d7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93d7-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d93d7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93d7-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d93d7-152">INPUTS</span></span>

### <span data-ttu-id="d93d7-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="d93d7-153">None</span></span>

## <span data-ttu-id="d93d7-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d93d7-154">OUTPUTS</span></span>

### <span data-ttu-id="d93d7-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d93d7-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="d93d7-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d93d7-156">NOTES</span></span>

## <span data-ttu-id="d93d7-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d93d7-157">RELATED LINKS</span></span>
