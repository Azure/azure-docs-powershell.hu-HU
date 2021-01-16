---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374316"
---
# <span data-ttu-id="eab39-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eab39-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="eab39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eab39-102">SYNOPSIS</span></span>
<span data-ttu-id="eab39-103">Eltávolítja a Edge Storage-fiók tártárolóját egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="eab39-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="eab39-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eab39-104">SYNTAX</span></span>

### <span data-ttu-id="eab39-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eab39-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eab39-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eab39-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eab39-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eab39-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eab39-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eab39-108">DESCRIPTION</span></span>
<span data-ttu-id="eab39-109">A **Remove-AzStackEdgeStorageContainer** parancsmag eltávolítja a Stack Edge-eszközön a Edge Storage-fiók társított tárolóját.</span><span class="sxs-lookup"><span data-stu-id="eab39-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="eab39-110">Megadhatja a paraméterként eltávolítható tároló tároló nevét.</span><span class="sxs-lookup"><span data-stu-id="eab39-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="eab39-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eab39-111">EXAMPLES</span></span>

### <span data-ttu-id="eab39-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="eab39-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="eab39-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eab39-113">PARAMETERS</span></span>

### <span data-ttu-id="eab39-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eab39-114">-AsJob</span></span>
<span data-ttu-id="eab39-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eab39-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eab39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab39-116">-DefaultProfile</span></span>
<span data-ttu-id="eab39-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eab39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab39-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eab39-118">-DeviceName</span></span>
<span data-ttu-id="eab39-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="eab39-119">Device Name</span></span>

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

### <span data-ttu-id="eab39-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eab39-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="eab39-121">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="eab39-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="eab39-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eab39-122">-InputObject</span></span>
<span data-ttu-id="eab39-123">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="eab39-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eab39-124">-Name</span><span class="sxs-lookup"><span data-stu-id="eab39-124">-Name</span></span>
<span data-ttu-id="eab39-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="eab39-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eab39-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eab39-126">-PassThru</span></span>
<span data-ttu-id="eab39-127">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="eab39-127">returns true if successful</span></span>

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

### <span data-ttu-id="eab39-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eab39-128">-ResourceGroupName</span></span>
<span data-ttu-id="eab39-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="eab39-129">Resource Group Name</span></span>

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

### <span data-ttu-id="eab39-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eab39-130">-ResourceId</span></span>
<span data-ttu-id="eab39-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="eab39-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="eab39-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eab39-132">-Confirm</span></span>
<span data-ttu-id="eab39-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eab39-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eab39-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eab39-134">-WhatIf</span></span>
<span data-ttu-id="eab39-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eab39-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eab39-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eab39-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eab39-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab39-137">CommonParameters</span></span>
<span data-ttu-id="eab39-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eab39-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab39-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eab39-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab39-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eab39-140">INPUTS</span></span>

### <span data-ttu-id="eab39-141">System.String</span><span class="sxs-lookup"><span data-stu-id="eab39-141">System.String</span></span>

### <span data-ttu-id="eab39-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eab39-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="eab39-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eab39-143">OUTPUTS</span></span>

### <span data-ttu-id="eab39-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eab39-144">System.Boolean</span></span>

## <span data-ttu-id="eab39-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eab39-145">NOTES</span></span>

## <span data-ttu-id="eab39-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eab39-146">RELATED LINKS</span></span>
