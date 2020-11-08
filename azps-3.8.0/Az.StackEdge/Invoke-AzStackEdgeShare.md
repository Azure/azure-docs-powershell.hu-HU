---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011044"
---
# <span data-ttu-id="1f470-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1f470-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="1f470-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f470-102">SYNOPSIS</span></span>
<span data-ttu-id="1f470-103">Meghívja a megosztás adott műveleteit.</span><span class="sxs-lookup"><span data-stu-id="1f470-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="1f470-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f470-104">SYNTAX</span></span>

### <span data-ttu-id="1f470-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f470-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f470-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f470-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f470-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f470-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f470-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f470-108">DESCRIPTION</span></span>
<span data-ttu-id="1f470-109">A **meghívó AzStackEdgeShare** parancsmag egy halom típusú eszközön lévő megosztás adatainak frissítésére hívja fel a művelet lépéseit.</span><span class="sxs-lookup"><span data-stu-id="1f470-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="1f470-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1f470-110">EXAMPLES</span></span>

### <span data-ttu-id="1f470-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1f470-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="1f470-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1f470-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="1f470-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f470-113">PARAMETERS</span></span>

### <span data-ttu-id="1f470-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f470-114">-AsJob</span></span>
<span data-ttu-id="1f470-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1f470-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f470-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f470-116">-DefaultProfile</span></span>
<span data-ttu-id="1f470-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f470-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f470-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1f470-118">-DeviceName</span></span>
<span data-ttu-id="1f470-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="1f470-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f470-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f470-120">-InputObject</span></span>
<span data-ttu-id="1f470-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="1f470-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f470-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f470-122">-Name</span></span>
<span data-ttu-id="1f470-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="1f470-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f470-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f470-124">-PassThru</span></span>
<span data-ttu-id="1f470-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="1f470-125">returns true if successful</span></span>

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

### <span data-ttu-id="1f470-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="1f470-126">-RefreshData</span></span>
<span data-ttu-id="1f470-127">A megosztási metaadatok frissítése a felhőből származó adatokkal</span><span class="sxs-lookup"><span data-stu-id="1f470-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="1f470-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f470-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f470-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1f470-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f470-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f470-130">-ResourceId</span></span>
<span data-ttu-id="1f470-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f470-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f470-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f470-132">-Confirm</span></span>
<span data-ttu-id="1f470-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f470-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f470-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f470-134">-WhatIf</span></span>
<span data-ttu-id="1f470-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f470-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f470-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f470-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f470-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f470-137">CommonParameters</span></span>
<span data-ttu-id="1f470-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f470-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f470-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f470-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f470-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f470-140">INPUTS</span></span>

### <span data-ttu-id="1f470-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1f470-141">System.String</span></span>

### <span data-ttu-id="1f470-142">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1f470-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="1f470-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f470-143">OUTPUTS</span></span>

### <span data-ttu-id="1f470-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f470-144">System.Boolean</span></span>

## <span data-ttu-id="1f470-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f470-145">NOTES</span></span>

## <span data-ttu-id="1f470-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f470-146">RELATED LINKS</span></span>
