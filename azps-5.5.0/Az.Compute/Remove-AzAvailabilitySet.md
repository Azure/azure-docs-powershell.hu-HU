---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144859"
---
# <span data-ttu-id="0b85e-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b85e-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="0b85e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b85e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b85e-103">Eltávolít egy rendelkezésre állási készletet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="0b85e-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="0b85e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b85e-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b85e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b85e-105">DESCRIPTION</span></span>
<span data-ttu-id="0b85e-106">A **Remove-AzAvailabilitySet** parancsmag eltávolít egy rendelkezésre állási készletet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="0b85e-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="0b85e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b85e-107">EXAMPLES</span></span>

### <span data-ttu-id="0b85e-108">1. példa: Elérhetőségi készlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0b85e-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0b85e-109">Ez a parancs eltávolít egy AvailabilitySet03 nevű elérhetőségi készletet az Erőforráscsoport11 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="0b85e-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="0b85e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b85e-110">PARAMETERS</span></span>

### <span data-ttu-id="0b85e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b85e-111">-AsJob</span></span>
<span data-ttu-id="0b85e-112">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="0b85e-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0b85e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b85e-113">-DefaultProfile</span></span>
<span data-ttu-id="0b85e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b85e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b85e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0b85e-115">-Force</span></span>
<span data-ttu-id="0b85e-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0b85e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b85e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0b85e-117">-Name</span></span>
<span data-ttu-id="0b85e-118">Az elérhetőségi készlet neve.</span><span class="sxs-lookup"><span data-stu-id="0b85e-118">The availability set name.</span></span>

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

### <span data-ttu-id="0b85e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b85e-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b85e-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b85e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0b85e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b85e-121">-Confirm</span></span>
<span data-ttu-id="0b85e-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0b85e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b85e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b85e-123">-WhatIf</span></span>
<span data-ttu-id="0b85e-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0b85e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b85e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b85e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b85e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b85e-126">CommonParameters</span></span>
<span data-ttu-id="0b85e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b85e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b85e-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b85e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b85e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b85e-129">INPUTS</span></span>

### <span data-ttu-id="0b85e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0b85e-130">System.String</span></span>

## <span data-ttu-id="0b85e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b85e-131">OUTPUTS</span></span>

### <span data-ttu-id="0b85e-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b85e-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0b85e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b85e-133">NOTES</span></span>

## <span data-ttu-id="0b85e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b85e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b85e-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b85e-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="0b85e-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b85e-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


