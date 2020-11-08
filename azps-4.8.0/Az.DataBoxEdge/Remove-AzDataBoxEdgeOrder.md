---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182351"
---
# <span data-ttu-id="54ba3-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="54ba3-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="54ba3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="54ba3-103">Eltávolítja az eszköz sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="54ba3-103">Removes the order for a device.</span></span>

## <span data-ttu-id="54ba3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54ba3-104">SYNTAX</span></span>

### <span data-ttu-id="54ba3-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54ba3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ba3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54ba3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ba3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54ba3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54ba3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="54ba3-108">DESCRIPTION</span></span>
<span data-ttu-id="54ba3-109">A **Remove-AzDataBoxEdgeOrder** parancsmag töröl egy meglévő sorrendet az adatmező Edge-eszközéhez.</span><span class="sxs-lookup"><span data-stu-id="54ba3-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="54ba3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="54ba3-110">EXAMPLES</span></span>

### <span data-ttu-id="54ba3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54ba3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="54ba3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54ba3-112">PARAMETERS</span></span>

### <span data-ttu-id="54ba3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54ba3-113">-AsJob</span></span>
<span data-ttu-id="54ba3-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="54ba3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54ba3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ba3-115">-DefaultProfile</span></span>
<span data-ttu-id="54ba3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54ba3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54ba3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="54ba3-117">-DeviceName</span></span>
<span data-ttu-id="54ba3-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="54ba3-118">Device Name</span></span>

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

### <span data-ttu-id="54ba3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54ba3-119">-InputObject</span></span>
<span data-ttu-id="54ba3-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="54ba3-120">Input Object</span></span>

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

### <span data-ttu-id="54ba3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54ba3-121">-PassThru</span></span>
<span data-ttu-id="54ba3-122">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="54ba3-122">returns true if successful</span></span>

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

### <span data-ttu-id="54ba3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54ba3-123">-ResourceGroupName</span></span>
<span data-ttu-id="54ba3-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="54ba3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="54ba3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54ba3-125">-ResourceId</span></span>
<span data-ttu-id="54ba3-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="54ba3-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="54ba3-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54ba3-127">-Confirm</span></span>
<span data-ttu-id="54ba3-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54ba3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54ba3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ba3-129">-WhatIf</span></span>
<span data-ttu-id="54ba3-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54ba3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54ba3-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54ba3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54ba3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ba3-132">CommonParameters</span></span>
<span data-ttu-id="54ba3-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54ba3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ba3-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="54ba3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ba3-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54ba3-135">INPUTS</span></span>

### <span data-ttu-id="54ba3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="54ba3-136">System.String</span></span>

### <span data-ttu-id="54ba3-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="54ba3-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="54ba3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54ba3-138">OUTPUTS</span></span>

### <span data-ttu-id="54ba3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="54ba3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="54ba3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54ba3-140">NOTES</span></span>

## <span data-ttu-id="54ba3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54ba3-141">RELATED LINKS</span></span>
