---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014573"
---
# <span data-ttu-id="99f91-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="99f91-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="99f91-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99f91-102">SYNOPSIS</span></span>
<span data-ttu-id="99f91-103">Eltávolít egy megosztást az eszközről.</span><span class="sxs-lookup"><span data-stu-id="99f91-103">Removes a share from the device.</span></span>

## <span data-ttu-id="99f91-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99f91-104">SYNTAX</span></span>

### <span data-ttu-id="99f91-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99f91-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f91-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f91-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f91-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f91-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f91-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="99f91-108">DESCRIPTION</span></span>
<span data-ttu-id="99f91-109">A **Remove-AzDataBoxEdgeEdgeShare** parancsmag eltávolítja a kapcsolódó peremhálózat-megosztásokat az adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="99f91-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="99f91-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99f91-110">EXAMPLES</span></span>

### <span data-ttu-id="99f91-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99f91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="99f91-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99f91-112">PARAMETERS</span></span>

### <span data-ttu-id="99f91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99f91-113">-AsJob</span></span>
<span data-ttu-id="99f91-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99f91-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99f91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f91-115">-DefaultProfile</span></span>
<span data-ttu-id="99f91-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99f91-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f91-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="99f91-117">-DeviceName</span></span>
<span data-ttu-id="99f91-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="99f91-118">Device Name</span></span>

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

### <span data-ttu-id="99f91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99f91-119">-InputObject</span></span>
<span data-ttu-id="99f91-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="99f91-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99f91-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99f91-121">-Name</span></span>
<span data-ttu-id="99f91-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="99f91-122">Resource Name</span></span>

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

### <span data-ttu-id="99f91-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99f91-123">-PassThru</span></span>
<span data-ttu-id="99f91-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="99f91-124">returns true if successful</span></span>

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

### <span data-ttu-id="99f91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f91-125">-ResourceGroupName</span></span>
<span data-ttu-id="99f91-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="99f91-126">Resource Group Name</span></span>

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

### <span data-ttu-id="99f91-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f91-127">-ResourceId</span></span>
<span data-ttu-id="99f91-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f91-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99f91-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99f91-129">-Confirm</span></span>
<span data-ttu-id="99f91-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99f91-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f91-131">-WhatIf</span></span>
<span data-ttu-id="99f91-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99f91-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99f91-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99f91-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f91-134">CommonParameters</span></span>
<span data-ttu-id="99f91-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99f91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f91-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99f91-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f91-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99f91-137">INPUTS</span></span>

### <span data-ttu-id="99f91-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99f91-138">System.String</span></span>

### <span data-ttu-id="99f91-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="99f91-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="99f91-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99f91-140">OUTPUTS</span></span>

### <span data-ttu-id="99f91-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99f91-141">System.Boolean</span></span>

## <span data-ttu-id="99f91-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99f91-142">NOTES</span></span>

## <span data-ttu-id="99f91-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99f91-143">RELATED LINKS</span></span>
