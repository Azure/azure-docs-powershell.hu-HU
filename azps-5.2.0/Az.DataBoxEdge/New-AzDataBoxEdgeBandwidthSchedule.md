---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361786"
---
# <span data-ttu-id="83455-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="83455-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="83455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83455-102">SYNOPSIS</span></span>
<span data-ttu-id="83455-103">Új sávszélesség-ütemezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="83455-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="83455-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83455-104">SYNTAX</span></span>

### <span data-ttu-id="83455-105">BandwidthParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83455-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83455-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="83455-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83455-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83455-107">DESCRIPTION</span></span>
<span data-ttu-id="83455-108">A **New-AzDataBoxEdgeBandwidthSchedule** parancsmag új sávszélesség-ütemezést hoz létre egy adatmező-edge-eszköz számára a sávszélesség-használat kezelése érdekében.</span><span class="sxs-lookup"><span data-stu-id="83455-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="83455-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83455-109">EXAMPLES</span></span>

### <span data-ttu-id="83455-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="83455-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="83455-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="83455-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="83455-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83455-112">PARAMETERS</span></span>

### <span data-ttu-id="83455-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83455-113">-AsJob</span></span>
<span data-ttu-id="83455-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="83455-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83455-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="83455-115">-Bandwidth</span></span>
<span data-ttu-id="83455-116">Bandwidth in Mbps</span><span class="sxs-lookup"><span data-stu-id="83455-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="83455-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="83455-117">-DaysOfWeek</span></span>
<span data-ttu-id="83455-118">Scheduled DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="83455-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="83455-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83455-119">-DefaultProfile</span></span>
<span data-ttu-id="83455-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83455-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83455-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="83455-121">-DeviceName</span></span>
<span data-ttu-id="83455-122">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="83455-122">Device Name</span></span>

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

### <span data-ttu-id="83455-123">-Name</span><span class="sxs-lookup"><span data-stu-id="83455-123">-Name</span></span>
<span data-ttu-id="83455-124">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="83455-124">Resource Name</span></span>

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

### <span data-ttu-id="83455-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83455-125">-ResourceGroupName</span></span>
<span data-ttu-id="83455-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="83455-126">Resource Group Name</span></span>

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

### <span data-ttu-id="83455-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="83455-127">-StartTime</span></span>
<span data-ttu-id="83455-128">Kezdési időpont ütemezése</span><span class="sxs-lookup"><span data-stu-id="83455-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="83455-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="83455-129">-StopTime</span></span>
<span data-ttu-id="83455-130">Ütemezési leállítási idő</span><span class="sxs-lookup"><span data-stu-id="83455-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="83455-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="83455-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="83455-132">A Korlátlan sávszélesség beállítása, ha a hamis értékre van állítva, az alapértelmezett érték 20 Mb/s</span><span class="sxs-lookup"><span data-stu-id="83455-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="83455-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83455-133">-Confirm</span></span>
<span data-ttu-id="83455-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="83455-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83455-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83455-135">-WhatIf</span></span>
<span data-ttu-id="83455-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="83455-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83455-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83455-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83455-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83455-138">CommonParameters</span></span>
<span data-ttu-id="83455-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83455-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83455-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83455-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83455-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83455-141">INPUTS</span></span>

### <span data-ttu-id="83455-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="83455-142">None</span></span>

## <span data-ttu-id="83455-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83455-143">OUTPUTS</span></span>

### <span data-ttu-id="83455-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="83455-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="83455-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83455-145">NOTES</span></span>

## <span data-ttu-id="83455-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83455-146">RELATED LINKS</span></span>
