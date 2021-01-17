---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480978"
---
# <span data-ttu-id="892cb-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="892cb-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="892cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="892cb-102">SYNOPSIS</span></span>
<span data-ttu-id="892cb-103">Közzéteheti egy tervrajz új verzióját.</span><span class="sxs-lookup"><span data-stu-id="892cb-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="892cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="892cb-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="892cb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="892cb-105">DESCRIPTION</span></span>
<span data-ttu-id="892cb-106">Közzéteheti a tervrajzdefiníció új verzióját.</span><span class="sxs-lookup"><span data-stu-id="892cb-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="892cb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="892cb-107">EXAMPLES</span></span>

### <span data-ttu-id="892cb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="892cb-108">Example 1</span></span>
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

<span data-ttu-id="892cb-109">Közzéteheti a tervrajzdefiníció új verzióját.</span><span class="sxs-lookup"><span data-stu-id="892cb-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="892cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="892cb-110">PARAMETERS</span></span>

### <span data-ttu-id="892cb-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="892cb-111">-Blueprint</span></span>
<span data-ttu-id="892cb-112">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="892cb-112">Blueprint object.</span></span>

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

### <span data-ttu-id="892cb-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="892cb-113">-ChangeNote</span></span>
<span data-ttu-id="892cb-114">A tervrajz ezen verziójának tartalmát leíró megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="892cb-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="892cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892cb-115">-DefaultProfile</span></span>
<span data-ttu-id="892cb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="892cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="892cb-117">-Version</span><span class="sxs-lookup"><span data-stu-id="892cb-117">-Version</span></span>
<span data-ttu-id="892cb-118">A tervrajz definíciójának verziója.</span><span class="sxs-lookup"><span data-stu-id="892cb-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="892cb-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="892cb-119">-Confirm</span></span>
<span data-ttu-id="892cb-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="892cb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="892cb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="892cb-121">-WhatIf</span></span>
<span data-ttu-id="892cb-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="892cb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="892cb-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="892cb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="892cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892cb-124">CommonParameters</span></span>
<span data-ttu-id="892cb-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892cb-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="892cb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892cb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="892cb-127">INPUTS</span></span>

### <span data-ttu-id="892cb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="892cb-128">System.String</span></span>

### <span data-ttu-id="892cb-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="892cb-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="892cb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="892cb-130">OUTPUTS</span></span>

### <span data-ttu-id="892cb-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="892cb-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="892cb-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="892cb-132">NOTES</span></span>

## <span data-ttu-id="892cb-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="892cb-133">RELATED LINKS</span></span>
