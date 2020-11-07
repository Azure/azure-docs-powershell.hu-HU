---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 7366e263f6106d2d332daab95f029d07c824aa90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667632"
---
# <span data-ttu-id="a721a-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a721a-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="a721a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a721a-102">SYNOPSIS</span></span>
<span data-ttu-id="a721a-103">A tervrajzok definíciójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a721a-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="a721a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a721a-104">SYNTAX</span></span>

### <span data-ttu-id="a721a-105">UpdateBlueprintBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a721a-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a721a-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a721a-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a721a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a721a-107">DESCRIPTION</span></span>
<span data-ttu-id="a721a-108">A terv definíciójának frissítése és mentése a megadott előfizetés vagy kezelés csoportban.</span><span class="sxs-lookup"><span data-stu-id="a721a-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="a721a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a721a-109">EXAMPLES</span></span>

### <span data-ttu-id="a721a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a721a-110">Example 1</span></span>
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

<span data-ttu-id="a721a-111">Új paraméterekkel frissítheti a terv definícióját.</span><span class="sxs-lookup"><span data-stu-id="a721a-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="a721a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a721a-112">PARAMETERS</span></span>

### <span data-ttu-id="a721a-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="a721a-113">-BlueprintFile</span></span>
<span data-ttu-id="a721a-114">A sablonban lévő JSON-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="a721a-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a721a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a721a-115">-DefaultProfile</span></span>
<span data-ttu-id="a721a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a721a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a721a-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a721a-117">-ManagementGroupId</span></span>
<span data-ttu-id="a721a-118">A felügyeleti csoport azonosítóját, ahol a tervrajz definícióját menti vagy menti a program.</span><span class="sxs-lookup"><span data-stu-id="a721a-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup, ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a721a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a721a-119">-Name</span></span>
<span data-ttu-id="a721a-120">Terv definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="a721a-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup, ImportBlueprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a721a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a721a-121">-SubscriptionId</span></span>
<span data-ttu-id="a721a-122">Az előfizetési azonosító, amelyben a terv definíciója vagy mentésére kerül.</span><span class="sxs-lookup"><span data-stu-id="a721a-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, ImportBlueprint, SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a721a-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a721a-123">-Confirm</span></span>
<span data-ttu-id="a721a-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a721a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a721a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a721a-125">-WhatIf</span></span>
<span data-ttu-id="a721a-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a721a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a721a-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a721a-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a721a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a721a-128">CommonParameters</span></span>
<span data-ttu-id="a721a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a721a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a721a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a721a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a721a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a721a-131">INPUTS</span></span>

### <span data-ttu-id="a721a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a721a-132">System.String</span></span>

## <span data-ttu-id="a721a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a721a-133">OUTPUTS</span></span>

### <span data-ttu-id="a721a-134">Microsoft. Azure. commands. Blueprint. models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="a721a-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="a721a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a721a-135">NOTES</span></span>

## <span data-ttu-id="a721a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a721a-136">RELATED LINKS</span></span>
