---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153538"
---
# <span data-ttu-id="664cf-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="664cf-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="664cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="664cf-102">SYNOPSIS</span></span>
<span data-ttu-id="664cf-103">Eltávolítja a Edge Storage-fiók tártárolóját egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="664cf-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="664cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="664cf-104">SYNTAX</span></span>

### <span data-ttu-id="664cf-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="664cf-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="664cf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="664cf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="664cf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="664cf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="664cf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="664cf-108">DESCRIPTION</span></span>
<span data-ttu-id="664cf-109">A **Remove-AzDataBoxEdgeStorageContainer** parancsmag eltávolítja a Edge Storage-fiók társított tárolóját egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="664cf-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="664cf-110">Megadhatja a paraméterként eltávolítható tároló nevét.</span><span class="sxs-lookup"><span data-stu-id="664cf-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="664cf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="664cf-111">EXAMPLES</span></span>

### <span data-ttu-id="664cf-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="664cf-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="664cf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="664cf-113">PARAMETERS</span></span>

### <span data-ttu-id="664cf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="664cf-114">-AsJob</span></span>
<span data-ttu-id="664cf-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="664cf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="664cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664cf-116">-DefaultProfile</span></span>
<span data-ttu-id="664cf-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="664cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="664cf-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="664cf-118">-DeviceName</span></span>
<span data-ttu-id="664cf-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="664cf-119">Device Name</span></span>

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

### <span data-ttu-id="664cf-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="664cf-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="664cf-121">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="664cf-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="664cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="664cf-122">-InputObject</span></span>
<span data-ttu-id="664cf-123">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="664cf-123">Input Object</span></span>

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

### <span data-ttu-id="664cf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="664cf-124">-Name</span></span>
<span data-ttu-id="664cf-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="664cf-125">Resource Name</span></span>

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

### <span data-ttu-id="664cf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="664cf-126">-PassThru</span></span>
<span data-ttu-id="664cf-127">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="664cf-127">returns true if successful</span></span>

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

### <span data-ttu-id="664cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="664cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="664cf-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="664cf-129">Resource Group Name</span></span>

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

### <span data-ttu-id="664cf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="664cf-130">-ResourceId</span></span>
<span data-ttu-id="664cf-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="664cf-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="664cf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="664cf-132">-Confirm</span></span>
<span data-ttu-id="664cf-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="664cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="664cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="664cf-134">-WhatIf</span></span>
<span data-ttu-id="664cf-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="664cf-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="664cf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="664cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="664cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664cf-137">CommonParameters</span></span>
<span data-ttu-id="664cf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="664cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664cf-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="664cf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664cf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="664cf-140">INPUTS</span></span>

### <span data-ttu-id="664cf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="664cf-141">System.String</span></span>

### <span data-ttu-id="664cf-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="664cf-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="664cf-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="664cf-143">OUTPUTS</span></span>

### <span data-ttu-id="664cf-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="664cf-144">System.Boolean</span></span>

## <span data-ttu-id="664cf-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="664cf-145">NOTES</span></span>

## <span data-ttu-id="664cf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="664cf-146">RELATED LINKS</span></span>
