---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934266"
---
# <span data-ttu-id="b47d2-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="b47d2-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="b47d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b47d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b47d2-103">Eltávolít egy gazdacsoportot.</span><span class="sxs-lookup"><span data-stu-id="b47d2-103">Removes a host group.</span></span>

## <span data-ttu-id="b47d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b47d2-104">SYNTAX</span></span>

### <span data-ttu-id="b47d2-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b47d2-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b47d2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b47d2-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b47d2-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b47d2-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b47d2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b47d2-108">DESCRIPTION</span></span>
<span data-ttu-id="b47d2-109">Ez a parancsmag töröl egy Gazdacsoportot</span><span class="sxs-lookup"><span data-stu-id="b47d2-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="b47d2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b47d2-110">EXAMPLES</span></span>

### <span data-ttu-id="b47d2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b47d2-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="b47d2-112">Ez a parancs be- és eltávolítja a megadott gazdacsoportot.</span><span class="sxs-lookup"><span data-stu-id="b47d2-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="b47d2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b47d2-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="b47d2-114">Ez a parancs eltávolítja a megadott gazdacsoportot.</span><span class="sxs-lookup"><span data-stu-id="b47d2-114">This command removes the given host group.</span></span>

## <span data-ttu-id="b47d2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b47d2-115">PARAMETERS</span></span>

### <span data-ttu-id="b47d2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b47d2-116">-AsJob</span></span>
<span data-ttu-id="b47d2-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b47d2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b47d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47d2-118">-DefaultProfile</span></span>
<span data-ttu-id="b47d2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b47d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b47d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b47d2-120">-InputObject</span></span>
<span data-ttu-id="b47d2-121">A gazdacsoport helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="b47d2-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b47d2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b47d2-122">-Name</span></span>
<span data-ttu-id="b47d2-123">A gazdacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b47d2-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b47d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b47d2-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b47d2-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b47d2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b47d2-126">-ResourceId</span></span>
<span data-ttu-id="b47d2-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b47d2-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b47d2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b47d2-128">-Confirm</span></span>
<span data-ttu-id="b47d2-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b47d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b47d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b47d2-130">-WhatIf</span></span>
<span data-ttu-id="b47d2-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b47d2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b47d2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b47d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b47d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47d2-133">CommonParameters</span></span>
<span data-ttu-id="b47d2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47d2-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b47d2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47d2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b47d2-136">INPUTS</span></span>

### <span data-ttu-id="b47d2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b47d2-137">System.String</span></span>

### <span data-ttu-id="b47d2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="b47d2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="b47d2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b47d2-139">OUTPUTS</span></span>

### <span data-ttu-id="b47d2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b47d2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b47d2-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b47d2-141">NOTES</span></span>

## <span data-ttu-id="b47d2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b47d2-142">RELATED LINKS</span></span>
