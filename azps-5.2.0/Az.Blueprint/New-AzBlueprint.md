---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 790a74ef5a296dbc90e9c1db16678b8c1bacf071
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331398"
---
# <span data-ttu-id="9689e-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="9689e-101">New-AzBlueprint</span></span>

## <span data-ttu-id="9689e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9689e-102">SYNOPSIS</span></span>
<span data-ttu-id="9689e-103">Hozzon létre egy új tervrajz-definíciót, és mentse azt a megadott előfizetésen vagy felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="9689e-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="9689e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9689e-104">SYNTAX</span></span>

### <span data-ttu-id="9689e-105">CreateBlueprintBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9689e-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9689e-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9689e-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9689e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9689e-107">DESCRIPTION</span></span>
<span data-ttu-id="9689e-108">Hozzon létre egy új tervrajz-definíciót.</span><span class="sxs-lookup"><span data-stu-id="9689e-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="9689e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9689e-109">EXAMPLES</span></span>

### <span data-ttu-id="9689e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9689e-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="9689e-111">Hozzon létre egy új tervrajz-definíciót a megadott előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="9689e-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="9689e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9689e-112">PARAMETERS</span></span>

### <span data-ttu-id="9689e-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="9689e-113">-BlueprintFile</span></span>
<span data-ttu-id="9689e-114">Path to a Blueprint JSON file on disk.</span><span class="sxs-lookup"><span data-stu-id="9689e-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="9689e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9689e-115">-DefaultProfile</span></span>
<span data-ttu-id="9689e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9689e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9689e-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9689e-117">-ManagementGroupId</span></span>
<span data-ttu-id="9689e-118">Management Group Id where the blueprint definition is or will be saved.</span><span class="sxs-lookup"><span data-stu-id="9689e-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9689e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9689e-119">-Name</span></span>
<span data-ttu-id="9689e-120">A tervrajz definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="9689e-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="9689e-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9689e-121">-SubscriptionId</span></span>
<span data-ttu-id="9689e-122">Előfizetés azonosítója, ahol a tervrajz definíciója mentve van vagy mentve lesz.</span><span class="sxs-lookup"><span data-stu-id="9689e-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9689e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9689e-123">-Confirm</span></span>
<span data-ttu-id="9689e-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9689e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9689e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9689e-125">-WhatIf</span></span>
<span data-ttu-id="9689e-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9689e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9689e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9689e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9689e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9689e-128">CommonParameters</span></span>
<span data-ttu-id="9689e-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9689e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9689e-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9689e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9689e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9689e-131">INPUTS</span></span>

### <span data-ttu-id="9689e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9689e-132">System.String</span></span>

## <span data-ttu-id="9689e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9689e-133">OUTPUTS</span></span>

### <span data-ttu-id="9689e-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="9689e-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="9689e-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9689e-135">NOTES</span></span>

## <span data-ttu-id="9689e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9689e-136">RELATED LINKS</span></span>
