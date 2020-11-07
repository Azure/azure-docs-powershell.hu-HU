---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: ccf76449bf2f7e904cbfe6e2507e067df7661dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667633"
---
# <span data-ttu-id="c0c53-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c0c53-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c0c53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0c53-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c53-103">Tervrajz-hozzárendelés eltávolítása az előfizetésből</span><span class="sxs-lookup"><span data-stu-id="c0c53-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="c0c53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0c53-104">SYNTAX</span></span>

### <span data-ttu-id="c0c53-105">DeleteBlueprintAssignmentByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0c53-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c53-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="c0c53-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c53-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0c53-107">DESCRIPTION</span></span>
<span data-ttu-id="c0c53-108">Előfizetéshez rendelt tervrajz eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c0c53-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="c0c53-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c0c53-109">EXAMPLES</span></span>

### <span data-ttu-id="c0c53-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0c53-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="c0c53-111">A megadott előfizetésből megadott név alapján megadott Blueprint-hozzárendelés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c0c53-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="c0c53-112">A parancsmag a parancs végrehajtása előtt kérni fogja a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0c53-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="c0c53-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0c53-113">PARAMETERS</span></span>

### <span data-ttu-id="c0c53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c53-114">-DefaultProfile</span></span>
<span data-ttu-id="c0c53-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0c53-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c53-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0c53-116">-InputObject</span></span>
<span data-ttu-id="c0c53-117">Terv hozzárendelés-objektuma.</span><span class="sxs-lookup"><span data-stu-id="c0c53-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c53-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0c53-118">-Name</span></span>
<span data-ttu-id="c0c53-119">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="c0c53-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c53-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0c53-120">-PassThru</span></span>
<span data-ttu-id="c0c53-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c0c53-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c0c53-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0c53-122">-SubscriptionId</span></span>
<span data-ttu-id="c0c53-123">Előfizetés azonosítója: a terv-hozzárendelés üzembe helyezése.</span><span class="sxs-lookup"><span data-stu-id="c0c53-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c53-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0c53-124">-Confirm</span></span>
<span data-ttu-id="c0c53-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0c53-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c53-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c53-126">-WhatIf</span></span>
<span data-ttu-id="c0c53-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0c53-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c53-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0c53-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c53-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c53-129">CommonParameters</span></span>
<span data-ttu-id="c0c53-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0c53-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c53-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c53-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c53-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c53-132">INPUTS</span></span>

### <span data-ttu-id="c0c53-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c0c53-133">System.String</span></span>

### <span data-ttu-id="c0c53-134">Microsoft. Azure. commands. Blueprint. models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="c0c53-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="c0c53-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c53-135">OUTPUTS</span></span>

### <span data-ttu-id="c0c53-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c0c53-136">System.Object</span></span>
## <span data-ttu-id="c0c53-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0c53-137">NOTES</span></span>

## <span data-ttu-id="c0c53-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0c53-138">RELATED LINKS</span></span>
