---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187208"
---
# <span data-ttu-id="5e69b-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5e69b-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="5e69b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e69b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e69b-103">Sávszélesség-ütemezés frissítése</span><span class="sxs-lookup"><span data-stu-id="5e69b-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="5e69b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e69b-104">SYNTAX</span></span>

### <span data-ttu-id="5e69b-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e69b-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e69b-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e69b-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e69b-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e69b-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e69b-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e69b-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e69b-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e69b-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5e69b-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e69b-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e69b-114">DESCRIPTION</span></span>
<span data-ttu-id="5e69b-115">A **set-AzStackEdgeBandwidthSchedule** parancsmag a halom szélén álló eszközök sávszélesség-ütemezését frissíti.</span><span class="sxs-lookup"><span data-stu-id="5e69b-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="5e69b-116">Példák</span><span class="sxs-lookup"><span data-stu-id="5e69b-116">EXAMPLES</span></span>

### <span data-ttu-id="5e69b-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5e69b-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="5e69b-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="5e69b-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="5e69b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e69b-119">PARAMETERS</span></span>

### <span data-ttu-id="5e69b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e69b-120">-AsJob</span></span>
<span data-ttu-id="5e69b-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5e69b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e69b-122">-Sávszélesség</span><span class="sxs-lookup"><span data-stu-id="5e69b-122">-Bandwidth</span></span>
<span data-ttu-id="5e69b-123">Sávszélesség a Mbps-ban</span><span class="sxs-lookup"><span data-stu-id="5e69b-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="5e69b-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="5e69b-124">-DaysOfWeek</span></span>
<span data-ttu-id="5e69b-125">Ütemezett DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="5e69b-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="5e69b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e69b-126">-DefaultProfile</span></span>
<span data-ttu-id="5e69b-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e69b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e69b-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5e69b-128">-DeviceName</span></span>
<span data-ttu-id="5e69b-129">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="5e69b-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e69b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e69b-130">-InputObject</span></span>
<span data-ttu-id="5e69b-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e69b-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e69b-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e69b-132">-Name</span></span>
<span data-ttu-id="5e69b-133">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="5e69b-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e69b-134">-ResourceGroupName</span></span>
<span data-ttu-id="5e69b-135">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5e69b-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e69b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e69b-136">-ResourceId</span></span>
<span data-ttu-id="5e69b-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e69b-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e69b-138">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="5e69b-138">-StartTime</span></span>
<span data-ttu-id="5e69b-139">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="5e69b-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="5e69b-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="5e69b-140">-StopTime</span></span>
<span data-ttu-id="5e69b-141">Befejezési idő ütemezése</span><span class="sxs-lookup"><span data-stu-id="5e69b-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="5e69b-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="5e69b-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="5e69b-143">Korlátlan sávszélességet ad meg</span><span class="sxs-lookup"><span data-stu-id="5e69b-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e69b-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e69b-144">-Confirm</span></span>
<span data-ttu-id="5e69b-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e69b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e69b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e69b-146">-WhatIf</span></span>
<span data-ttu-id="5e69b-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e69b-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e69b-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e69b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e69b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e69b-149">CommonParameters</span></span>
<span data-ttu-id="5e69b-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e69b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e69b-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5e69b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e69b-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e69b-152">INPUTS</span></span>

### <span data-ttu-id="5e69b-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e69b-153">None</span></span>

## <span data-ttu-id="5e69b-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e69b-154">OUTPUTS</span></span>

### <span data-ttu-id="5e69b-155">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5e69b-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="5e69b-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e69b-156">NOTES</span></span>

## <span data-ttu-id="5e69b-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e69b-157">RELATED LINKS</span></span>