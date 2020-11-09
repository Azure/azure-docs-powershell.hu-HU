---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302381"
---
# <span data-ttu-id="47ebe-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="47ebe-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="47ebe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="47ebe-103">Meghívja a megosztás adott műveleteit.</span><span class="sxs-lookup"><span data-stu-id="47ebe-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="47ebe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47ebe-104">SYNTAX</span></span>

### <span data-ttu-id="47ebe-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47ebe-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47ebe-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47ebe-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ebe-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47ebe-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47ebe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="47ebe-108">DESCRIPTION</span></span>
<span data-ttu-id="47ebe-109">A **meghívó AzStackEdgeShare** parancsmag egy halom típusú eszközön lévő megosztás adatainak frissítésére hívja fel a művelet lépéseit.</span><span class="sxs-lookup"><span data-stu-id="47ebe-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="47ebe-110">Példák</span><span class="sxs-lookup"><span data-stu-id="47ebe-110">EXAMPLES</span></span>

### <span data-ttu-id="47ebe-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47ebe-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="47ebe-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="47ebe-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="47ebe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47ebe-113">PARAMETERS</span></span>

### <span data-ttu-id="47ebe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47ebe-114">-AsJob</span></span>
<span data-ttu-id="47ebe-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="47ebe-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47ebe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ebe-116">-DefaultProfile</span></span>
<span data-ttu-id="47ebe-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47ebe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ebe-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="47ebe-118">-DeviceName</span></span>
<span data-ttu-id="47ebe-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="47ebe-119">Device Name</span></span>

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

### <span data-ttu-id="47ebe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47ebe-120">-InputObject</span></span>
<span data-ttu-id="47ebe-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="47ebe-121">Input Object</span></span>

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

### <span data-ttu-id="47ebe-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47ebe-122">-Name</span></span>
<span data-ttu-id="47ebe-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="47ebe-123">Resource Name</span></span>

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

### <span data-ttu-id="47ebe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47ebe-124">-PassThru</span></span>
<span data-ttu-id="47ebe-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="47ebe-125">returns true if successful</span></span>

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

### <span data-ttu-id="47ebe-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="47ebe-126">-RefreshData</span></span>
<span data-ttu-id="47ebe-127">A megosztási metaadatok frissítése a felhőből származó adatokkal</span><span class="sxs-lookup"><span data-stu-id="47ebe-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="47ebe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ebe-128">-ResourceGroupName</span></span>
<span data-ttu-id="47ebe-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="47ebe-129">Resource Group Name</span></span>

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

### <span data-ttu-id="47ebe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47ebe-130">-ResourceId</span></span>
<span data-ttu-id="47ebe-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="47ebe-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="47ebe-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47ebe-132">-Confirm</span></span>
<span data-ttu-id="47ebe-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47ebe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ebe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ebe-134">-WhatIf</span></span>
<span data-ttu-id="47ebe-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47ebe-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47ebe-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47ebe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ebe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ebe-137">CommonParameters</span></span>
<span data-ttu-id="47ebe-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47ebe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ebe-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47ebe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ebe-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47ebe-140">INPUTS</span></span>

### <span data-ttu-id="47ebe-141">System. String</span><span class="sxs-lookup"><span data-stu-id="47ebe-141">System.String</span></span>

### <span data-ttu-id="47ebe-142">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="47ebe-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="47ebe-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47ebe-143">OUTPUTS</span></span>

### <span data-ttu-id="47ebe-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47ebe-144">System.Boolean</span></span>

## <span data-ttu-id="47ebe-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47ebe-145">NOTES</span></span>

## <span data-ttu-id="47ebe-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47ebe-146">RELATED LINKS</span></span>
