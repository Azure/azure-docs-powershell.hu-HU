---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 11a2aeffc1ab3bb170b2e8543d9fd5d0300e3ce5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011171"
---
# <span data-ttu-id="6507c-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="6507c-101">New-AzBlueprint</span></span>

## <span data-ttu-id="6507c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6507c-102">SYNOPSIS</span></span>
<span data-ttu-id="6507c-103">Hozzon létre egy új tervrajz-definíciót, és mentse azt a megadott előfizetés vagy kezelési csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="6507c-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="6507c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6507c-104">SYNTAX</span></span>

### <span data-ttu-id="6507c-105">CreateBlueprintBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6507c-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6507c-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6507c-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6507c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6507c-107">DESCRIPTION</span></span>
<span data-ttu-id="6507c-108">Új Blueprint-definíció létrehozása</span><span class="sxs-lookup"><span data-stu-id="6507c-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="6507c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6507c-109">EXAMPLES</span></span>

### <span data-ttu-id="6507c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6507c-110">Example 1</span></span>
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

<span data-ttu-id="6507c-111">Új Blueprint-definíció létrehozása a megadott előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="6507c-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="6507c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6507c-112">PARAMETERS</span></span>

### <span data-ttu-id="6507c-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="6507c-113">-BlueprintFile</span></span>
<span data-ttu-id="6507c-114">A sablonban lévő JSON-fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="6507c-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6507c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6507c-115">-DefaultProfile</span></span>
<span data-ttu-id="6507c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6507c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6507c-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="6507c-117">-ManagementGroupId</span></span>
<span data-ttu-id="6507c-118">A felügyeleti csoport azonosítóját, ahol a tervrajz definícióját menti vagy menti a program.</span><span class="sxs-lookup"><span data-stu-id="6507c-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6507c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6507c-119">-Name</span></span>
<span data-ttu-id="6507c-120">Terv definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="6507c-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6507c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6507c-121">-SubscriptionId</span></span>
<span data-ttu-id="6507c-122">Az előfizetési azonosító, amelyben a terv definíciója vagy mentésére kerül.</span><span class="sxs-lookup"><span data-stu-id="6507c-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6507c-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6507c-123">-Confirm</span></span>
<span data-ttu-id="6507c-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6507c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6507c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6507c-125">-WhatIf</span></span>
<span data-ttu-id="6507c-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6507c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6507c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6507c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6507c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6507c-128">CommonParameters</span></span>
<span data-ttu-id="6507c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6507c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6507c-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6507c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6507c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6507c-131">INPUTS</span></span>

### <span data-ttu-id="6507c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6507c-132">System.String</span></span>

## <span data-ttu-id="6507c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6507c-133">OUTPUTS</span></span>

### <span data-ttu-id="6507c-134">Microsoft. Azure. commands. Blueprint. models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="6507c-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="6507c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6507c-135">NOTES</span></span>

## <span data-ttu-id="6507c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6507c-136">RELATED LINKS</span></span>
