---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012319"
---
# <span data-ttu-id="26365-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="26365-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="26365-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26365-102">SYNOPSIS</span></span>
<span data-ttu-id="26365-103">Eltávolítja az eszköz sorrendjét.</span><span class="sxs-lookup"><span data-stu-id="26365-103">Removes the order for a device.</span></span>

## <span data-ttu-id="26365-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26365-104">SYNTAX</span></span>

### <span data-ttu-id="26365-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26365-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26365-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26365-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26365-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26365-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26365-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="26365-108">DESCRIPTION</span></span>
<span data-ttu-id="26365-109">A **Remove-AzStackEdgeOrder** parancsmag törli a meglévő sorrendet a halom szélén álló eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="26365-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="26365-110">Példák</span><span class="sxs-lookup"><span data-stu-id="26365-110">EXAMPLES</span></span>

### <span data-ttu-id="26365-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26365-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="26365-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26365-112">PARAMETERS</span></span>

### <span data-ttu-id="26365-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26365-113">-AsJob</span></span>
<span data-ttu-id="26365-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="26365-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26365-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26365-115">-DefaultProfile</span></span>
<span data-ttu-id="26365-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26365-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26365-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="26365-117">-DeviceName</span></span>
<span data-ttu-id="26365-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="26365-118">Device Name</span></span>

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

### <span data-ttu-id="26365-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26365-119">-InputObject</span></span>
<span data-ttu-id="26365-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="26365-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26365-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26365-121">-PassThru</span></span>
<span data-ttu-id="26365-122">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="26365-122">returns true if successful</span></span>

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

### <span data-ttu-id="26365-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26365-123">-ResourceGroupName</span></span>
<span data-ttu-id="26365-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="26365-124">Resource Group Name</span></span>

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

### <span data-ttu-id="26365-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26365-125">-ResourceId</span></span>
<span data-ttu-id="26365-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="26365-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="26365-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26365-127">-Confirm</span></span>
<span data-ttu-id="26365-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26365-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26365-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26365-129">-WhatIf</span></span>
<span data-ttu-id="26365-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26365-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26365-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26365-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26365-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26365-132">CommonParameters</span></span>
<span data-ttu-id="26365-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26365-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26365-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26365-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26365-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26365-135">INPUTS</span></span>

### <span data-ttu-id="26365-136">System. String</span><span class="sxs-lookup"><span data-stu-id="26365-136">System.String</span></span>

### <span data-ttu-id="26365-137">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="26365-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="26365-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26365-138">OUTPUTS</span></span>

### <span data-ttu-id="26365-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="26365-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="26365-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26365-140">NOTES</span></span>

## <span data-ttu-id="26365-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26365-141">RELATED LINKS</span></span>
