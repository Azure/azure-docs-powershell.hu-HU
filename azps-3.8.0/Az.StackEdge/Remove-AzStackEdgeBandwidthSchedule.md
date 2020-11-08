---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010736"
---
# <span data-ttu-id="b0dbe-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dbe-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b0dbe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="b0dbe-103">Sávszélesség-ütemterv eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b0dbe-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="b0dbe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0dbe-104">SYNTAX</span></span>

### <span data-ttu-id="b0dbe-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0dbe-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dbe-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0dbe-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dbe-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0dbe-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0dbe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0dbe-108">DESCRIPTION</span></span>
<span data-ttu-id="b0dbe-109">A **Remove-AzStackEdgeBandwidthSchedule** parancsmag eltávolítja egy halom Edge-eszköz sávszélességének ütemtervét.</span><span class="sxs-lookup"><span data-stu-id="b0dbe-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="b0dbe-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b0dbe-110">EXAMPLES</span></span>

### <span data-ttu-id="b0dbe-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b0dbe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="b0dbe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0dbe-112">PARAMETERS</span></span>

### <span data-ttu-id="b0dbe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0dbe-113">-AsJob</span></span>
<span data-ttu-id="b0dbe-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b0dbe-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0dbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0dbe-115">-DefaultProfile</span></span>
<span data-ttu-id="b0dbe-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0dbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0dbe-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b0dbe-117">-DeviceName</span></span>
<span data-ttu-id="b0dbe-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="b0dbe-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dbe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0dbe-119">-InputObject</span></span>
<span data-ttu-id="b0dbe-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="b0dbe-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dbe-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b0dbe-121">-Name</span></span>
<span data-ttu-id="b0dbe-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b0dbe-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dbe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0dbe-123">-PassThru</span></span>
<span data-ttu-id="b0dbe-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="b0dbe-124">returns true if successful</span></span>

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

### <span data-ttu-id="b0dbe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0dbe-125">-ResourceGroupName</span></span>
<span data-ttu-id="b0dbe-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b0dbe-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dbe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0dbe-127">-ResourceId</span></span>
<span data-ttu-id="b0dbe-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0dbe-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dbe-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0dbe-129">-Confirm</span></span>
<span data-ttu-id="b0dbe-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0dbe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0dbe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0dbe-131">-WhatIf</span></span>
<span data-ttu-id="b0dbe-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0dbe-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0dbe-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0dbe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0dbe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0dbe-134">CommonParameters</span></span>
<span data-ttu-id="b0dbe-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0dbe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0dbe-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b0dbe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0dbe-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0dbe-137">INPUTS</span></span>

### <span data-ttu-id="b0dbe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b0dbe-138">System.String</span></span>

### <span data-ttu-id="b0dbe-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b0dbe-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b0dbe-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0dbe-140">OUTPUTS</span></span>

### <span data-ttu-id="b0dbe-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0dbe-141">System.Boolean</span></span>

## <span data-ttu-id="b0dbe-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0dbe-142">NOTES</span></span>

## <span data-ttu-id="b0dbe-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0dbe-143">RELATED LINKS</span></span>
