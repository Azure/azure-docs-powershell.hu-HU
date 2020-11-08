---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 176ef6d90fed93a65da10a1f1174f2b81f1fe094
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011596"
---
# <span data-ttu-id="96bde-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="96bde-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="96bde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96bde-102">SYNOPSIS</span></span>
<span data-ttu-id="96bde-103">Az Azure Security Center díjszabási küszöbértékét kapja meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="96bde-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="96bde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96bde-104">SYNTAX</span></span>

### <span data-ttu-id="96bde-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96bde-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96bde-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="96bde-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96bde-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="96bde-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96bde-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="96bde-108">DESCRIPTION</span></span>
<span data-ttu-id="96bde-109">Az Azure biztonsági központ árképzési rétege hatóköre, ezzel a parancsmaggal megadhatja a beállított árképzési szinteket.</span><span class="sxs-lookup"><span data-stu-id="96bde-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="96bde-110">Az előfizetés árazási szintje tartalmazza az összes erőforráscsoport-csoportot.</span><span class="sxs-lookup"><span data-stu-id="96bde-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="96bde-111">Az erőforráscsoport árazási szintje felülbírálja az előfizetés árazási rétegét.</span><span class="sxs-lookup"><span data-stu-id="96bde-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="96bde-112">Példák</span><span class="sxs-lookup"><span data-stu-id="96bde-112">EXAMPLES</span></span>

### <span data-ttu-id="96bde-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="96bde-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="96bde-114">Beilleszti az előfizetéshez tartozó összes beállított árazási szintet, valamint az alatta lévő erőforráscsoportokat.</span><span class="sxs-lookup"><span data-stu-id="96bde-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="96bde-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="96bde-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="96bde-116">Az "myService1" erőforráscsoport konfigurált árazási rétegét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="96bde-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="96bde-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96bde-117">PARAMETERS</span></span>

### <span data-ttu-id="96bde-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96bde-118">-DefaultProfile</span></span>
<span data-ttu-id="96bde-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96bde-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96bde-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96bde-120">-Name</span></span>
<span data-ttu-id="96bde-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="96bde-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96bde-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96bde-122">-ResourceId</span></span>
<span data-ttu-id="96bde-123">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="96bde-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96bde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96bde-124">CommonParameters</span></span>
<span data-ttu-id="96bde-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96bde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96bde-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96bde-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96bde-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96bde-127">INPUTS</span></span>

### <span data-ttu-id="96bde-128">System. String</span><span class="sxs-lookup"><span data-stu-id="96bde-128">System.String</span></span>

## <span data-ttu-id="96bde-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96bde-129">OUTPUTS</span></span>

### <span data-ttu-id="96bde-130">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="96bde-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="96bde-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96bde-131">NOTES</span></span>

## <span data-ttu-id="96bde-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96bde-132">RELATED LINKS</span></span>
