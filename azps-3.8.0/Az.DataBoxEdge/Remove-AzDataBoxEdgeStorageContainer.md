---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014571"
---
# <span data-ttu-id="4050d-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4050d-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="4050d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4050d-102">SYNOPSIS</span></span>
<span data-ttu-id="4050d-103">Eltávolítja az eszközön az Edge Storage (tároló) tárterületet tároló tárolót.</span><span class="sxs-lookup"><span data-stu-id="4050d-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="4050d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4050d-104">SYNTAX</span></span>

### <span data-ttu-id="4050d-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4050d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4050d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4050d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4050d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4050d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4050d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4050d-108">DESCRIPTION</span></span>
<span data-ttu-id="4050d-109">A **Remove-AzDataBoxEdgeStorageContainer** parancsmagja eltávolítja az Edge Storage-fiókhoz tartozó tároló tárolót az adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="4050d-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="4050d-110">Megadhatja annak a tároló-tárolónak a nevét, amelyet paraméterként szeretne eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="4050d-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="4050d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4050d-111">EXAMPLES</span></span>

### <span data-ttu-id="4050d-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4050d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="4050d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4050d-113">PARAMETERS</span></span>

### <span data-ttu-id="4050d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4050d-114">-AsJob</span></span>
<span data-ttu-id="4050d-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4050d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4050d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4050d-116">-DefaultProfile</span></span>
<span data-ttu-id="4050d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4050d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4050d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4050d-118">-DeviceName</span></span>
<span data-ttu-id="4050d-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="4050d-119">Device Name</span></span>

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

### <span data-ttu-id="4050d-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4050d-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="4050d-121">Létező EdgeStorageAccount-név megadása</span><span class="sxs-lookup"><span data-stu-id="4050d-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4050d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4050d-122">-InputObject</span></span>
<span data-ttu-id="4050d-123">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="4050d-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4050d-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4050d-124">-Name</span></span>
<span data-ttu-id="4050d-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4050d-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4050d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4050d-126">-PassThru</span></span>
<span data-ttu-id="4050d-127">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="4050d-127">returns true if successful</span></span>

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

### <span data-ttu-id="4050d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4050d-128">-ResourceGroupName</span></span>
<span data-ttu-id="4050d-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4050d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="4050d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4050d-130">-ResourceId</span></span>
<span data-ttu-id="4050d-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4050d-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="4050d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4050d-132">-Confirm</span></span>
<span data-ttu-id="4050d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4050d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4050d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4050d-134">-WhatIf</span></span>
<span data-ttu-id="4050d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4050d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4050d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4050d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4050d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4050d-137">CommonParameters</span></span>
<span data-ttu-id="4050d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4050d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4050d-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4050d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4050d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4050d-140">INPUTS</span></span>

### <span data-ttu-id="4050d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4050d-141">System.String</span></span>

### <span data-ttu-id="4050d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4050d-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="4050d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4050d-143">OUTPUTS</span></span>

### <span data-ttu-id="4050d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4050d-144">System.Boolean</span></span>

## <span data-ttu-id="4050d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4050d-145">NOTES</span></span>

## <span data-ttu-id="4050d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4050d-146">RELATED LINKS</span></span>
