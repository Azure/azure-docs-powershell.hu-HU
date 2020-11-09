---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298796"
---
# <span data-ttu-id="f9290-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9290-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f9290-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9290-102">SYNOPSIS</span></span>
<span data-ttu-id="f9290-103">Meghatározott műveletek meghívása a tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="f9290-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="f9290-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9290-104">SYNTAX</span></span>

### <span data-ttu-id="f9290-105">InvokeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9290-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9290-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9290-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9290-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9290-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9290-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9290-108">DESCRIPTION</span></span>
<span data-ttu-id="f9290-109">Az **AzDataBoxEdgeStorageContainer** parancsmag műveleteket kezdeményez az adatdobozos eszközön tárolt tárterület adatainak frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f9290-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="f9290-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f9290-110">EXAMPLES</span></span>

### <span data-ttu-id="f9290-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f9290-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="f9290-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f9290-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="f9290-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9290-113">PARAMETERS</span></span>

### <span data-ttu-id="f9290-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9290-114">-AsJob</span></span>
<span data-ttu-id="f9290-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f9290-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9290-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9290-116">-DefaultProfile</span></span>
<span data-ttu-id="f9290-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9290-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9290-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f9290-118">-DeviceName</span></span>
<span data-ttu-id="f9290-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="f9290-119">Device Name</span></span>

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

### <span data-ttu-id="f9290-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f9290-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="f9290-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f9290-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9290-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9290-122">-InputObject</span></span>
<span data-ttu-id="f9290-123">Meglévő EdgeStorageAccount-objektum nyújtása</span><span class="sxs-lookup"><span data-stu-id="f9290-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9290-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9290-124">-Name</span></span>
<span data-ttu-id="f9290-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f9290-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9290-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9290-126">-PassThru</span></span>
<span data-ttu-id="f9290-127">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="f9290-127">returns true if successful</span></span>

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

### <span data-ttu-id="f9290-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="f9290-128">-RefreshData</span></span>
<span data-ttu-id="f9290-129">Tároló metaadatainak frissítése a felhőből származó adatokkal</span><span class="sxs-lookup"><span data-stu-id="f9290-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="f9290-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9290-130">-ResourceGroupName</span></span>
<span data-ttu-id="f9290-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f9290-131">Resource Group Name</span></span>

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

### <span data-ttu-id="f9290-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9290-132">-ResourceId</span></span>
<span data-ttu-id="f9290-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9290-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9290-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9290-134">-Confirm</span></span>
<span data-ttu-id="f9290-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9290-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9290-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9290-136">-WhatIf</span></span>
<span data-ttu-id="f9290-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9290-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9290-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9290-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9290-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9290-139">CommonParameters</span></span>
<span data-ttu-id="f9290-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9290-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9290-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f9290-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9290-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9290-142">INPUTS</span></span>

### <span data-ttu-id="f9290-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f9290-143">System.String</span></span>

### <span data-ttu-id="f9290-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9290-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f9290-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9290-145">OUTPUTS</span></span>

### <span data-ttu-id="f9290-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9290-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f9290-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9290-147">NOTES</span></span>

## <span data-ttu-id="f9290-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9290-148">RELATED LINKS</span></span>
