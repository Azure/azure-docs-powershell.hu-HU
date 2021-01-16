---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358678"
---
# <span data-ttu-id="93e43-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="93e43-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="93e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e43-102">SYNOPSIS</span></span>
<span data-ttu-id="93e43-103">Frissíti a sávszélesség-ütemezést.</span><span class="sxs-lookup"><span data-stu-id="93e43-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="93e43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93e43-104">SYNTAX</span></span>

### <span data-ttu-id="93e43-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93e43-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e43-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e43-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93e43-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="93e43-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e43-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="93e43-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e43-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e43-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e43-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="93e43-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e43-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="93e43-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e43-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="93e43-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e43-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="93e43-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e43-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93e43-114">DESCRIPTION</span></span>
<span data-ttu-id="93e43-115">A **Set-AzStackEdgeBandwidthSchedule** parancsmag frissíti a Stack Edge-es eszközök sávszélesség-ütemezését.</span><span class="sxs-lookup"><span data-stu-id="93e43-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="93e43-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93e43-116">EXAMPLES</span></span>

### <span data-ttu-id="93e43-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="93e43-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="93e43-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="93e43-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="93e43-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e43-119">PARAMETERS</span></span>

### <span data-ttu-id="93e43-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93e43-120">-AsJob</span></span>
<span data-ttu-id="93e43-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="93e43-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93e43-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="93e43-122">-Bandwidth</span></span>
<span data-ttu-id="93e43-123">Bandwidth in Mbps</span><span class="sxs-lookup"><span data-stu-id="93e43-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="93e43-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="93e43-124">-DaysOfWeek</span></span>
<span data-ttu-id="93e43-125">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="93e43-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="93e43-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e43-126">-DefaultProfile</span></span>
<span data-ttu-id="93e43-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93e43-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e43-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="93e43-128">-DeviceName</span></span>
<span data-ttu-id="93e43-129">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="93e43-129">Device Name</span></span>

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

### <span data-ttu-id="93e43-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93e43-130">-InputObject</span></span>
<span data-ttu-id="93e43-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="93e43-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="93e43-132">-Name</span><span class="sxs-lookup"><span data-stu-id="93e43-132">-Name</span></span>
<span data-ttu-id="93e43-133">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="93e43-133">Resource Name</span></span>

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

### <span data-ttu-id="93e43-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e43-134">-ResourceGroupName</span></span>
<span data-ttu-id="93e43-135">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="93e43-135">Resource Group Name</span></span>

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

### <span data-ttu-id="93e43-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93e43-136">-ResourceId</span></span>
<span data-ttu-id="93e43-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="93e43-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="93e43-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="93e43-138">-StartTime</span></span>
<span data-ttu-id="93e43-139">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="93e43-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="93e43-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="93e43-140">-StopTime</span></span>
<span data-ttu-id="93e43-141">Ütemezési leállítási idő</span><span class="sxs-lookup"><span data-stu-id="93e43-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="93e43-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="93e43-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="93e43-143">Korlátlan sávszélességet fog beállítani</span><span class="sxs-lookup"><span data-stu-id="93e43-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="93e43-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93e43-144">-Confirm</span></span>
<span data-ttu-id="93e43-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93e43-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e43-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e43-146">-WhatIf</span></span>
<span data-ttu-id="93e43-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93e43-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93e43-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93e43-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e43-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e43-149">CommonParameters</span></span>
<span data-ttu-id="93e43-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e43-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e43-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93e43-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e43-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93e43-152">INPUTS</span></span>

### <span data-ttu-id="93e43-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="93e43-153">None</span></span>

## <span data-ttu-id="93e43-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93e43-154">OUTPUTS</span></span>

### <span data-ttu-id="93e43-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="93e43-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="93e43-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93e43-156">NOTES</span></span>

## <span data-ttu-id="93e43-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93e43-157">RELATED LINKS</span></span>
