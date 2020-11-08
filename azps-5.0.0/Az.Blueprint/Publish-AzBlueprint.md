---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186098"
---
# <span data-ttu-id="220cc-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="220cc-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="220cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="220cc-102">SYNOPSIS</span></span>
<span data-ttu-id="220cc-103">A tervezet új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="220cc-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="220cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="220cc-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="220cc-105">DESCRIPTION</span></span>
<span data-ttu-id="220cc-106">A Blueprint-definíciók új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="220cc-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="220cc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="220cc-107">EXAMPLES</span></span>

### <span data-ttu-id="220cc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="220cc-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="220cc-109">A Blueprint-definíciók új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="220cc-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="220cc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="220cc-110">PARAMETERS</span></span>

### <span data-ttu-id="220cc-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="220cc-111">-Blueprint</span></span>
<span data-ttu-id="220cc-112">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="220cc-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="220cc-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="220cc-113">-ChangeNote</span></span>
<span data-ttu-id="220cc-114">Megjegyzések a Blueprint-verzió tartalmának leírásához.</span><span class="sxs-lookup"><span data-stu-id="220cc-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="220cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220cc-115">-DefaultProfile</span></span>
<span data-ttu-id="220cc-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="220cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="220cc-117">-Verzió</span><span class="sxs-lookup"><span data-stu-id="220cc-117">-Version</span></span>
<span data-ttu-id="220cc-118">A terv definíciójának verziója.</span><span class="sxs-lookup"><span data-stu-id="220cc-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="220cc-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="220cc-119">-Confirm</span></span>
<span data-ttu-id="220cc-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="220cc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="220cc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220cc-121">-WhatIf</span></span>
<span data-ttu-id="220cc-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="220cc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="220cc-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="220cc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="220cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220cc-124">CommonParameters</span></span>
<span data-ttu-id="220cc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="220cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220cc-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="220cc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220cc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="220cc-127">INPUTS</span></span>

### <span data-ttu-id="220cc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="220cc-128">System.String</span></span>

### <span data-ttu-id="220cc-129">Microsoft. Azure. commands. Blueprint. models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="220cc-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="220cc-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="220cc-130">OUTPUTS</span></span>

### <span data-ttu-id="220cc-131">Microsoft. Azure. commands. Blueprint. models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="220cc-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="220cc-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="220cc-132">NOTES</span></span>

## <span data-ttu-id="220cc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="220cc-133">RELATED LINKS</span></span>