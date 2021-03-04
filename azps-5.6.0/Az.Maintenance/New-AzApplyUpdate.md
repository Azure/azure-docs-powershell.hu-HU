---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 535282da3f294acc7b8e4db321266748144155ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918785"
---
# <span data-ttu-id="ae174-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="ae174-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="ae174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae174-102">SYNOPSIS</span></span>
<span data-ttu-id="ae174-103">Karbantartási frissítések alkalmazása az erőforrásra</span><span class="sxs-lookup"><span data-stu-id="ae174-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="ae174-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae174-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae174-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae174-105">DESCRIPTION</span></span>
<span data-ttu-id="ae174-106">Karbantartási frissítések alkalmazása az erőforrásra</span><span class="sxs-lookup"><span data-stu-id="ae174-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="ae174-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae174-107">EXAMPLES</span></span>

### <span data-ttu-id="ae174-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ae174-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="ae174-109">Karbantartási frissítések alkalmazása az erőforrásra</span><span class="sxs-lookup"><span data-stu-id="ae174-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="ae174-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae174-110">PARAMETERS</span></span>

### <span data-ttu-id="ae174-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae174-111">-AsJob</span></span>
<span data-ttu-id="ae174-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ae174-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae174-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae174-113">-DefaultProfile</span></span>
<span data-ttu-id="ae174-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae174-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae174-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="ae174-115">-ProviderName</span></span>
<span data-ttu-id="ae174-116">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="ae174-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae174-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae174-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae174-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ae174-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="ae174-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ae174-119">-ResourceName</span></span>
<span data-ttu-id="ae174-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ae174-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae174-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="ae174-121">-ResourceParentName</span></span>
<span data-ttu-id="ae174-122">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ae174-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae174-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="ae174-123">-ResourceParentType</span></span>
<span data-ttu-id="ae174-124">A szülőerőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="ae174-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae174-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ae174-125">-ResourceType</span></span>
<span data-ttu-id="ae174-126">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="ae174-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae174-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae174-127">-Confirm</span></span>
<span data-ttu-id="ae174-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ae174-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae174-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae174-129">-WhatIf</span></span>
<span data-ttu-id="ae174-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ae174-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae174-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae174-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae174-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae174-132">CommonParameters</span></span>
<span data-ttu-id="ae174-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae174-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae174-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae174-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae174-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae174-135">INPUTS</span></span>

### <span data-ttu-id="ae174-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ae174-136">System.String</span></span>

## <span data-ttu-id="ae174-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae174-137">OUTPUTS</span></span>

### <span data-ttu-id="ae174-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="ae174-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="ae174-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae174-139">NOTES</span></span>

## <span data-ttu-id="ae174-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae174-140">RELATED LINKS</span></span>
