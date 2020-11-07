---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847642"
---
# <span data-ttu-id="9abc6-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="9abc6-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="9abc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9abc6-102">SYNOPSIS</span></span>
<span data-ttu-id="9abc6-103">Egy állomás csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9abc6-103">Removes a host group.</span></span>

## <span data-ttu-id="9abc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9abc6-104">SYNTAX</span></span>

### <span data-ttu-id="9abc6-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9abc6-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abc6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9abc6-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abc6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9abc6-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9abc6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9abc6-108">DESCRIPTION</span></span>
<span data-ttu-id="9abc6-109">Ez a parancsmag egy állomás-csoportot fog törölni</span><span class="sxs-lookup"><span data-stu-id="9abc6-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="9abc6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9abc6-110">EXAMPLES</span></span>

### <span data-ttu-id="9abc6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9abc6-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="9abc6-112">Ez a parancs beilleszti és eltávolítja a megadott állomásvezérlő-csoportot.</span><span class="sxs-lookup"><span data-stu-id="9abc6-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="9abc6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9abc6-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="9abc6-114">Ez a parancs eltávolítja a megadott állomásvezérlő-csoportot.</span><span class="sxs-lookup"><span data-stu-id="9abc6-114">This command removes the given host group.</span></span>

## <span data-ttu-id="9abc6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9abc6-115">PARAMETERS</span></span>

### <span data-ttu-id="9abc6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9abc6-116">-AsJob</span></span>
<span data-ttu-id="9abc6-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9abc6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9abc6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abc6-118">-DefaultProfile</span></span>
<span data-ttu-id="9abc6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9abc6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9abc6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9abc6-120">-InputObject</span></span>
<span data-ttu-id="9abc6-121">A Host csoport helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="9abc6-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="9abc6-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9abc6-122">-Name</span></span>
<span data-ttu-id="9abc6-123">A Host csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9abc6-123">The name of the host group.</span></span>

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

### <span data-ttu-id="9abc6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9abc6-124">-ResourceGroupName</span></span>
<span data-ttu-id="9abc6-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9abc6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="9abc6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9abc6-126">-ResourceId</span></span>
<span data-ttu-id="9abc6-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9abc6-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="9abc6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9abc6-128">-Confirm</span></span>
<span data-ttu-id="9abc6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9abc6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abc6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abc6-130">-WhatIf</span></span>
<span data-ttu-id="9abc6-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9abc6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abc6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9abc6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abc6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abc6-133">CommonParameters</span></span>
<span data-ttu-id="9abc6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9abc6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abc6-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9abc6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abc6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9abc6-136">INPUTS</span></span>

### <span data-ttu-id="9abc6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9abc6-137">System.String</span></span>

### <span data-ttu-id="9abc6-138">Microsoft. Azure. commands. számítási. Automation. models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="9abc6-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="9abc6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9abc6-139">OUTPUTS</span></span>

### <span data-ttu-id="9abc6-140">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9abc6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9abc6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9abc6-141">NOTES</span></span>

## <span data-ttu-id="9abc6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9abc6-142">RELATED LINKS</span></span>
