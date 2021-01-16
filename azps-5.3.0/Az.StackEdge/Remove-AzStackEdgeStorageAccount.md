---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376374"
---
# <span data-ttu-id="aeff0-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aeff0-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="aeff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeff0-102">SYNOPSIS</span></span>
<span data-ttu-id="aeff0-103">Eltávolítja egy eszköz Edge Storage-fiókját.</span><span class="sxs-lookup"><span data-stu-id="aeff0-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="aeff0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aeff0-104">SYNTAX</span></span>

### <span data-ttu-id="aeff0-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aeff0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeff0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeff0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeff0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeff0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeff0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aeff0-108">DESCRIPTION</span></span>
<span data-ttu-id="aeff0-109">A **Remove-AzStackEdgeStorageAccount** parancsmag eltávolítja a stack edge-es eszközökhez tartozó Edge Storage-fiókot.</span><span class="sxs-lookup"><span data-stu-id="aeff0-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="aeff0-110">Megadhatja a parancsmagban paraméterként eltávolítható Edge Storage-fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="aeff0-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="aeff0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aeff0-111">EXAMPLES</span></span>

### <span data-ttu-id="aeff0-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="aeff0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="aeff0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeff0-113">PARAMETERS</span></span>

### <span data-ttu-id="aeff0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aeff0-114">-AsJob</span></span>
<span data-ttu-id="aeff0-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aeff0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aeff0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeff0-116">-DefaultProfile</span></span>
<span data-ttu-id="aeff0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aeff0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeff0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="aeff0-118">-DeviceName</span></span>
<span data-ttu-id="aeff0-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="aeff0-119">Device Name</span></span>

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

### <span data-ttu-id="aeff0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aeff0-120">-InputObject</span></span>
<span data-ttu-id="aeff0-121">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="aeff0-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aeff0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aeff0-122">-Name</span></span>
<span data-ttu-id="aeff0-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="aeff0-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeff0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aeff0-124">-PassThru</span></span>
<span data-ttu-id="aeff0-125">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="aeff0-125">returns true if successful</span></span>

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

### <span data-ttu-id="aeff0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeff0-126">-ResourceGroupName</span></span>
<span data-ttu-id="aeff0-127">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="aeff0-127">Resource Group Name</span></span>

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

### <span data-ttu-id="aeff0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aeff0-128">-ResourceId</span></span>
<span data-ttu-id="aeff0-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="aeff0-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="aeff0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aeff0-130">-Confirm</span></span>
<span data-ttu-id="aeff0-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aeff0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeff0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeff0-132">-WhatIf</span></span>
<span data-ttu-id="aeff0-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aeff0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeff0-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aeff0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeff0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeff0-135">CommonParameters</span></span>
<span data-ttu-id="aeff0-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeff0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeff0-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aeff0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeff0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aeff0-138">INPUTS</span></span>

### <span data-ttu-id="aeff0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="aeff0-139">System.String</span></span>

### <span data-ttu-id="aeff0-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aeff0-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="aeff0-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aeff0-141">OUTPUTS</span></span>

### <span data-ttu-id="aeff0-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aeff0-142">System.Boolean</span></span>

## <span data-ttu-id="aeff0-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aeff0-143">NOTES</span></span>

## <span data-ttu-id="aeff0-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aeff0-144">RELATED LINKS</span></span>
