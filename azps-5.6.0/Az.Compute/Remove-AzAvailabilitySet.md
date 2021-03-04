---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: a4b4e5048e4d11a5b376650b94520232f10b29bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937097"
---
# <span data-ttu-id="238d3-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="238d3-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="238d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="238d3-102">SYNOPSIS</span></span>
<span data-ttu-id="238d3-103">Eltávolít egy rendelkezésre állási készletet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="238d3-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="238d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="238d3-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="238d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="238d3-105">DESCRIPTION</span></span>
<span data-ttu-id="238d3-106">A **Remove-AzAvailabilitySet** parancsmag eltávolít egy rendelkezésre állási készletet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="238d3-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="238d3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="238d3-107">EXAMPLES</span></span>

### <span data-ttu-id="238d3-108">1. példa: Elérhetőségi készlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="238d3-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="238d3-109">Ez a parancs eltávolít egy AvailabilitySet03 nevű elérhetőségi készletet az Erőforráscsoport11 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="238d3-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="238d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="238d3-110">PARAMETERS</span></span>

### <span data-ttu-id="238d3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="238d3-111">-AsJob</span></span>
<span data-ttu-id="238d3-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="238d3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="238d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238d3-113">-DefaultProfile</span></span>
<span data-ttu-id="238d3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="238d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="238d3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="238d3-115">-Force</span></span>
<span data-ttu-id="238d3-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="238d3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238d3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="238d3-117">-Name</span></span>
<span data-ttu-id="238d3-118">Az elérhetőségi készlet neve.</span><span class="sxs-lookup"><span data-stu-id="238d3-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="238d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="238d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="238d3-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="238d3-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="238d3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="238d3-121">-Confirm</span></span>
<span data-ttu-id="238d3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="238d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="238d3-123">-WhatIf</span></span>
<span data-ttu-id="238d3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="238d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="238d3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="238d3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238d3-126">CommonParameters</span></span>
<span data-ttu-id="238d3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="238d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238d3-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="238d3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238d3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="238d3-129">INPUTS</span></span>

### <span data-ttu-id="238d3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="238d3-130">System.String</span></span>

## <span data-ttu-id="238d3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="238d3-131">OUTPUTS</span></span>

### <span data-ttu-id="238d3-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="238d3-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="238d3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="238d3-133">NOTES</span></span>

## <span data-ttu-id="238d3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="238d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="238d3-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="238d3-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="238d3-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="238d3-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


