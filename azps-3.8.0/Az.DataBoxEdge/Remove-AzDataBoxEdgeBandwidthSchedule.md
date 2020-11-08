---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014575"
---
# <span data-ttu-id="9511c-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9511c-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="9511c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9511c-102">SYNOPSIS</span></span>
<span data-ttu-id="9511c-103">Sávszélesség-ütemterv eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9511c-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="9511c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9511c-104">SYNTAX</span></span>

### <span data-ttu-id="9511c-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9511c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9511c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9511c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9511c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9511c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9511c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9511c-108">DESCRIPTION</span></span>
<span data-ttu-id="9511c-109">A **Remove-AzDataBoxEdgeBandwidthSchedule** parancsmag eltávolítja az adatmező peremhálózati eszközének sávszélesség-ütemezését.</span><span class="sxs-lookup"><span data-stu-id="9511c-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="9511c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9511c-110">EXAMPLES</span></span>

### <span data-ttu-id="9511c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9511c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="9511c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9511c-112">PARAMETERS</span></span>

### <span data-ttu-id="9511c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9511c-113">-AsJob</span></span>
<span data-ttu-id="9511c-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9511c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9511c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9511c-115">-DefaultProfile</span></span>
<span data-ttu-id="9511c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9511c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9511c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9511c-117">-DeviceName</span></span>
<span data-ttu-id="9511c-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="9511c-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9511c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9511c-119">-InputObject</span></span>
<span data-ttu-id="9511c-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="9511c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9511c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9511c-121">-Name</span></span>
<span data-ttu-id="9511c-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9511c-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9511c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9511c-123">-PassThru</span></span>
<span data-ttu-id="9511c-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="9511c-124">returns true if successful</span></span>

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

### <span data-ttu-id="9511c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9511c-125">-ResourceGroupName</span></span>
<span data-ttu-id="9511c-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9511c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9511c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9511c-127">-ResourceId</span></span>
<span data-ttu-id="9511c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9511c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="9511c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9511c-129">-Confirm</span></span>
<span data-ttu-id="9511c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9511c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9511c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9511c-131">-WhatIf</span></span>
<span data-ttu-id="9511c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9511c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9511c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9511c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9511c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9511c-134">CommonParameters</span></span>
<span data-ttu-id="9511c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9511c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9511c-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9511c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9511c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9511c-137">INPUTS</span></span>

### <span data-ttu-id="9511c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9511c-138">System.String</span></span>

### <span data-ttu-id="9511c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9511c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="9511c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9511c-140">OUTPUTS</span></span>

### <span data-ttu-id="9511c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9511c-141">System.Boolean</span></span>

## <span data-ttu-id="9511c-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9511c-142">NOTES</span></span>

## <span data-ttu-id="9511c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9511c-143">RELATED LINKS</span></span>
