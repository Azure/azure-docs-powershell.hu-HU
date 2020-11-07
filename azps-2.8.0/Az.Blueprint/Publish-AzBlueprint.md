---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 5286b8953a9f28c5e63fe176f19d9d885e9c1d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667634"
---
# <span data-ttu-id="a37cd-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a37cd-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="a37cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a37cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a37cd-103">A tervezet új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="a37cd-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="a37cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a37cd-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a37cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a37cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a37cd-106">A Blueprint-definíciók új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="a37cd-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="a37cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a37cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a37cd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a37cd-108">Example 1</span></span>
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
<span data-ttu-id="a37cd-109">A Blueprint-definíciók új verziójának közzététele</span><span class="sxs-lookup"><span data-stu-id="a37cd-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="a37cd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a37cd-110">PARAMETERS</span></span>

### <span data-ttu-id="a37cd-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a37cd-111">-Blueprint</span></span>
<span data-ttu-id="a37cd-112">Blueprint objektum.</span><span class="sxs-lookup"><span data-stu-id="a37cd-112">Blueprint object.</span></span>

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

### <span data-ttu-id="a37cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37cd-113">-DefaultProfile</span></span>
<span data-ttu-id="a37cd-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a37cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a37cd-115">-Verzió</span><span class="sxs-lookup"><span data-stu-id="a37cd-115">-Version</span></span>
<span data-ttu-id="a37cd-116">A terv definíciójának verziója.</span><span class="sxs-lookup"><span data-stu-id="a37cd-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="a37cd-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="a37cd-117">-ChangeNote</span></span>
<span data-ttu-id="a37cd-118">Megjegyzések a Blueprint-verzió tartalmának leírásához.</span><span class="sxs-lookup"><span data-stu-id="a37cd-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="a37cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37cd-119">CommonParameters</span></span>
<span data-ttu-id="a37cd-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a37cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a37cd-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a37cd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37cd-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a37cd-122">INPUTS</span></span>

### <span data-ttu-id="a37cd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a37cd-123">System.String</span></span>

### <span data-ttu-id="a37cd-124">Microsoft. Azure. commands. Blueprint. models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="a37cd-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="a37cd-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a37cd-125">OUTPUTS</span></span>

### <span data-ttu-id="a37cd-126">Microsoft. Azure. commands. Blueprint. models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="a37cd-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="a37cd-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a37cd-127">NOTES</span></span>

## <span data-ttu-id="a37cd-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a37cd-128">RELATED LINKS</span></span>
