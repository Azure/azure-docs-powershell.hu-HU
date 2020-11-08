---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010991"
---
# <span data-ttu-id="bc37e-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="bc37e-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="bc37e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc37e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc37e-103">A tervezet új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="bc37e-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="bc37e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc37e-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc37e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc37e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc37e-106">A Blueprint-definíciók új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="bc37e-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="bc37e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc37e-107">EXAMPLES</span></span>

### <span data-ttu-id="bc37e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bc37e-108">Example 1</span></span>
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
<span data-ttu-id="bc37e-109">A Blueprint-definíciók új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="bc37e-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="bc37e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc37e-110">PARAMETERS</span></span>

### <span data-ttu-id="bc37e-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="bc37e-111">-Blueprint</span></span>
<span data-ttu-id="bc37e-112">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="bc37e-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc37e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc37e-113">-DefaultProfile</span></span>
<span data-ttu-id="bc37e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc37e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc37e-115">-Verzió</span><span class="sxs-lookup"><span data-stu-id="bc37e-115">-Version</span></span>
<span data-ttu-id="bc37e-116">A terv definíciójának verziója.</span><span class="sxs-lookup"><span data-stu-id="bc37e-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="bc37e-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="bc37e-117">-ChangeNote</span></span>
<span data-ttu-id="bc37e-118">Megjegyzések a Blueprint-verzió tartalmának leírásához.</span><span class="sxs-lookup"><span data-stu-id="bc37e-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="bc37e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc37e-119">CommonParameters</span></span>
<span data-ttu-id="bc37e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc37e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bc37e-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc37e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc37e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc37e-122">INPUTS</span></span>

### <span data-ttu-id="bc37e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bc37e-123">System.String</span></span>

### <span data-ttu-id="bc37e-124">Microsoft. Azure. commands. Blueprint. models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="bc37e-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="bc37e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc37e-125">OUTPUTS</span></span>

### <span data-ttu-id="bc37e-126">Microsoft. Azure. commands. Blueprint. models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="bc37e-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="bc37e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc37e-127">NOTES</span></span>

## <span data-ttu-id="bc37e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc37e-128">RELATED LINKS</span></span>
