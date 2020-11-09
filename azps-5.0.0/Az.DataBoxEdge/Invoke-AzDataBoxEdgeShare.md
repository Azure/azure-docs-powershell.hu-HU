---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298799"
---
# <span data-ttu-id="ad717-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ad717-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="ad717-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad717-102">SYNOPSIS</span></span>
<span data-ttu-id="ad717-103">Meghívja a megosztás adott műveleteit.</span><span class="sxs-lookup"><span data-stu-id="ad717-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="ad717-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad717-104">SYNTAX</span></span>

### <span data-ttu-id="ad717-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad717-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad717-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad717-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad717-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad717-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad717-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad717-108">DESCRIPTION</span></span>
<span data-ttu-id="ad717-109">A **meghívó AzDataBoxEdgeShare** parancsmag az adatmező szélén lévő eszközön lévő megosztási adatok frissítésére szolgáló műveletre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="ad717-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="ad717-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ad717-110">EXAMPLES</span></span>

### <span data-ttu-id="ad717-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad717-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="ad717-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ad717-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="ad717-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad717-113">PARAMETERS</span></span>

### <span data-ttu-id="ad717-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad717-114">-AsJob</span></span>
<span data-ttu-id="ad717-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ad717-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad717-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad717-116">-DefaultProfile</span></span>
<span data-ttu-id="ad717-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad717-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad717-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ad717-118">-DeviceName</span></span>
<span data-ttu-id="ad717-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="ad717-119">Device Name</span></span>

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

### <span data-ttu-id="ad717-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad717-120">-InputObject</span></span>
<span data-ttu-id="ad717-121">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="ad717-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad717-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad717-122">-Name</span></span>
<span data-ttu-id="ad717-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="ad717-123">Resource Name</span></span>

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

### <span data-ttu-id="ad717-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad717-124">-PassThru</span></span>
<span data-ttu-id="ad717-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="ad717-125">returns true if successful</span></span>

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

### <span data-ttu-id="ad717-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="ad717-126">-RefreshData</span></span>
<span data-ttu-id="ad717-127">A megosztási metaadatok frissítése a felhőből származó adatokkal</span><span class="sxs-lookup"><span data-stu-id="ad717-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="ad717-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad717-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad717-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ad717-129">Resource Group Name</span></span>

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

### <span data-ttu-id="ad717-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad717-130">-ResourceId</span></span>
<span data-ttu-id="ad717-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad717-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="ad717-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad717-132">-Confirm</span></span>
<span data-ttu-id="ad717-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad717-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad717-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad717-134">-WhatIf</span></span>
<span data-ttu-id="ad717-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad717-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad717-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad717-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad717-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad717-137">CommonParameters</span></span>
<span data-ttu-id="ad717-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad717-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad717-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad717-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad717-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad717-140">INPUTS</span></span>

### <span data-ttu-id="ad717-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad717-141">System.String</span></span>

### <span data-ttu-id="ad717-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ad717-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="ad717-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad717-143">OUTPUTS</span></span>

### <span data-ttu-id="ad717-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad717-144">System.Boolean</span></span>

## <span data-ttu-id="ad717-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad717-145">NOTES</span></span>

## <span data-ttu-id="ad717-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad717-146">RELATED LINKS</span></span>
