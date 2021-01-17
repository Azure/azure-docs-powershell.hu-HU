---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480976"
---
# <span data-ttu-id="b39a0-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="b39a0-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="b39a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b39a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b39a0-103">A tervrajz definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b39a0-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="b39a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b39a0-104">SYNTAX</span></span>

### <span data-ttu-id="b39a0-105">UpdateBlueprintBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b39a0-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b39a0-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b39a0-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b39a0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b39a0-107">DESCRIPTION</span></span>
<span data-ttu-id="b39a0-108">Frissítse a tervdefiníciót, és mentse a megadott előfizetés vagy felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="b39a0-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="b39a0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b39a0-109">EXAMPLES</span></span>

### <span data-ttu-id="b39a0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b39a0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="b39a0-111">A tervrajz definíciójának frissítése új paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="b39a0-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="b39a0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b39a0-112">PARAMETERS</span></span>

### <span data-ttu-id="b39a0-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="b39a0-113">-BlueprintFile</span></span>
<span data-ttu-id="b39a0-114">Path to a Blueprint JSON file on disk.</span><span class="sxs-lookup"><span data-stu-id="b39a0-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b39a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39a0-115">-DefaultProfile</span></span>
<span data-ttu-id="b39a0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b39a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b39a0-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b39a0-117">-ManagementGroupId</span></span>
<span data-ttu-id="b39a0-118">Management Group Id where the blueprint definition is or will be saved.</span><span class="sxs-lookup"><span data-stu-id="b39a0-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b39a0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b39a0-119">-Name</span></span>
<span data-ttu-id="b39a0-120">A tervrajz definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b39a0-120">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b39a0-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b39a0-121">-SubscriptionId</span></span>
<span data-ttu-id="b39a0-122">Előfizetés azonosítója, ahol a tervrajz definíciója mentve van vagy mentve lesz.</span><span class="sxs-lookup"><span data-stu-id="b39a0-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b39a0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b39a0-123">-Confirm</span></span>
<span data-ttu-id="b39a0-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b39a0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b39a0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b39a0-125">-WhatIf</span></span>
<span data-ttu-id="b39a0-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b39a0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b39a0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b39a0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b39a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39a0-128">CommonParameters</span></span>
<span data-ttu-id="b39a0-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b39a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39a0-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b39a0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39a0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b39a0-131">INPUTS</span></span>

### <span data-ttu-id="b39a0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b39a0-132">System.String</span></span>

## <span data-ttu-id="b39a0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b39a0-133">OUTPUTS</span></span>

### <span data-ttu-id="b39a0-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="b39a0-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="b39a0-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b39a0-135">NOTES</span></span>

## <span data-ttu-id="b39a0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b39a0-136">RELATED LINKS</span></span>
