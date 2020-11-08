---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: b3a99d286c0efcf76dee0c71d8d3b5f4e704ca40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014569"
---
# <span data-ttu-id="11efb-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="11efb-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="11efb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11efb-102">SYNOPSIS</span></span>
<span data-ttu-id="11efb-103">Eltávolítja az eszközhöz tartozó IoT szerepkört.</span><span class="sxs-lookup"><span data-stu-id="11efb-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="11efb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11efb-104">SYNTAX</span></span>

### <span data-ttu-id="11efb-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11efb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11efb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11efb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11efb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11efb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11efb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="11efb-108">DESCRIPTION</span></span>
<span data-ttu-id="11efb-109">A **Remove-AzDataBoxEdgeRole** parancsmag eltávolítja a kapcsolódó IoT szerepkört az adatmező Edge-eszközéhez.</span><span class="sxs-lookup"><span data-stu-id="11efb-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="11efb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="11efb-110">EXAMPLES</span></span>

### <span data-ttu-id="11efb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11efb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="11efb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11efb-112">PARAMETERS</span></span>

### <span data-ttu-id="11efb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11efb-113">-AsJob</span></span>
<span data-ttu-id="11efb-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="11efb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11efb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11efb-115">-DefaultProfile</span></span>
<span data-ttu-id="11efb-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11efb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11efb-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="11efb-117">-DeviceName</span></span>
<span data-ttu-id="11efb-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="11efb-118">Device Name</span></span>

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

### <span data-ttu-id="11efb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11efb-119">-InputObject</span></span>
<span data-ttu-id="11efb-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="11efb-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11efb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11efb-121">-Name</span></span>
<span data-ttu-id="11efb-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="11efb-122">Resource Name</span></span>

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

### <span data-ttu-id="11efb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11efb-123">-PassThru</span></span>
<span data-ttu-id="11efb-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="11efb-124">returns true if successful</span></span>

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

### <span data-ttu-id="11efb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11efb-125">-ResourceGroupName</span></span>
<span data-ttu-id="11efb-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="11efb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="11efb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11efb-127">-ResourceId</span></span>
<span data-ttu-id="11efb-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="11efb-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="11efb-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11efb-129">-Confirm</span></span>
<span data-ttu-id="11efb-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11efb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11efb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11efb-131">-WhatIf</span></span>
<span data-ttu-id="11efb-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11efb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11efb-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11efb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11efb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11efb-134">CommonParameters</span></span>
<span data-ttu-id="11efb-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11efb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11efb-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11efb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11efb-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11efb-137">INPUTS</span></span>

### <span data-ttu-id="11efb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="11efb-138">System.String</span></span>

### <span data-ttu-id="11efb-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="11efb-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="11efb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11efb-140">OUTPUTS</span></span>

### <span data-ttu-id="11efb-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="11efb-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="11efb-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11efb-142">NOTES</span></span>

## <span data-ttu-id="11efb-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11efb-143">RELATED LINKS</span></span>
