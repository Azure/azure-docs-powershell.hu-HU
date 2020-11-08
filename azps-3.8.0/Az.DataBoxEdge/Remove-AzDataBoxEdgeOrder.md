---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014572"
---
# <span data-ttu-id="5c33d-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="5c33d-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="5c33d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c33d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c33d-103">Eltávolítja az eszköz sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="5c33d-103">Removes the order for a device.</span></span>

## <span data-ttu-id="5c33d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c33d-104">SYNTAX</span></span>

### <span data-ttu-id="5c33d-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c33d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c33d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c33d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c33d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c33d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c33d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c33d-108">DESCRIPTION</span></span>
<span data-ttu-id="5c33d-109">A **Remove-AzDataBoxEdgeOrder** parancsmag töröl egy meglévő sorrendet az adatmező Edge-eszközéhez.</span><span class="sxs-lookup"><span data-stu-id="5c33d-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="5c33d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5c33d-110">EXAMPLES</span></span>

### <span data-ttu-id="5c33d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5c33d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="5c33d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c33d-112">PARAMETERS</span></span>

### <span data-ttu-id="5c33d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c33d-113">-AsJob</span></span>
<span data-ttu-id="5c33d-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5c33d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c33d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c33d-115">-DefaultProfile</span></span>
<span data-ttu-id="5c33d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c33d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c33d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5c33d-117">-DeviceName</span></span>
<span data-ttu-id="5c33d-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="5c33d-118">Device Name</span></span>

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

### <span data-ttu-id="5c33d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c33d-119">-InputObject</span></span>
<span data-ttu-id="5c33d-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="5c33d-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c33d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c33d-121">-PassThru</span></span>
<span data-ttu-id="5c33d-122">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="5c33d-122">returns true if successful</span></span>

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

### <span data-ttu-id="5c33d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c33d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5c33d-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5c33d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5c33d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c33d-125">-ResourceId</span></span>
<span data-ttu-id="5c33d-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c33d-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="5c33d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5c33d-127">-Confirm</span></span>
<span data-ttu-id="5c33d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5c33d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c33d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c33d-129">-WhatIf</span></span>
<span data-ttu-id="5c33d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5c33d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c33d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c33d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c33d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c33d-132">CommonParameters</span></span>
<span data-ttu-id="5c33d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c33d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c33d-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5c33d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c33d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c33d-135">INPUTS</span></span>

### <span data-ttu-id="5c33d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5c33d-136">System.String</span></span>

### <span data-ttu-id="5c33d-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="5c33d-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="5c33d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c33d-138">OUTPUTS</span></span>

### <span data-ttu-id="5c33d-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="5c33d-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="5c33d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c33d-140">NOTES</span></span>

## <span data-ttu-id="5c33d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c33d-141">RELATED LINKS</span></span>
