---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501315"
---
# <span data-ttu-id="c6f38-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c6f38-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="c6f38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6f38-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f38-103">Előfizetési definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c6f38-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6f38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6f38-104">SYNTAX</span></span>

### <span data-ttu-id="c6f38-105">Előfizetés-definíció létrehozása</span><span class="sxs-lookup"><span data-stu-id="c6f38-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="c6f38-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6f38-106">DESCRIPTION</span></span>
<span data-ttu-id="c6f38-107">A **New-AzureRmSubscriptionDefinition** parancsmag előfizetési definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c6f38-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="c6f38-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c6f38-108">EXAMPLES</span></span>

### <span data-ttu-id="c6f38-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6f38-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="c6f38-110">Előfizetési definíciót hoz létre alapértelmezett előfizetéses megjelenítendő névvel.</span><span class="sxs-lookup"><span data-stu-id="c6f38-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="c6f38-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="c6f38-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="c6f38-112">Előfizetési definíciót hoz létre egy egyéni előfizetéses megjelenítendő névvel.</span><span class="sxs-lookup"><span data-stu-id="c6f38-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="c6f38-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6f38-113">PARAMETERS</span></span>

### <span data-ttu-id="c6f38-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6f38-114">-Name</span></span>
<span data-ttu-id="c6f38-115">A létrehozandó előfizetés-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="c6f38-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f38-116">-OfferType</span><span class="sxs-lookup"><span data-stu-id="c6f38-116">-OfferType</span></span>
<span data-ttu-id="c6f38-117">A mögöttes előfizetés létrehozásakor használandó ajánlat típusa.</span><span class="sxs-lookup"><span data-stu-id="c6f38-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f38-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="c6f38-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="c6f38-119">Az előfizetési definíció alapjául szolgáló előfizetés létrehozásakor használandó megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="c6f38-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f38-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f38-120">CommonParameters</span></span>
<span data-ttu-id="c6f38-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6f38-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f38-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f38-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f38-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6f38-123">INPUTS</span></span>

### <span data-ttu-id="c6f38-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="c6f38-124">None</span></span>

## <span data-ttu-id="c6f38-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6f38-125">OUTPUTS</span></span>

### <span data-ttu-id="c6f38-126">Microsoft. Azure. Command. SubscriptionDefinition. models. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c6f38-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="c6f38-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6f38-127">NOTES</span></span>

## <span data-ttu-id="c6f38-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6f38-128">RELATED LINKS</span></span>

