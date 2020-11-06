---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492738"
---
# <span data-ttu-id="b359a-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b359a-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="b359a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b359a-102">SYNOPSIS</span></span>
<span data-ttu-id="b359a-103">Az Azure Security Center díjszabási küszöbértékét kapja meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="b359a-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b359a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b359a-104">SYNTAX</span></span>

### <span data-ttu-id="b359a-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b359a-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b359a-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b359a-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b359a-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="b359a-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b359a-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b359a-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b359a-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b359a-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b359a-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="b359a-110">DESCRIPTION</span></span>
<span data-ttu-id="b359a-111">Az Azure biztonsági központ árképzési rétege hatóköre, ezzel a parancsmaggal megadhatja a beállított árképzési szinteket.</span><span class="sxs-lookup"><span data-stu-id="b359a-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="b359a-112">Az előfizetés árazási szintje tartalmazza az összes erőforráscsoport-csoportot.</span><span class="sxs-lookup"><span data-stu-id="b359a-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="b359a-113">Az erőforráscsoport árazási szintje felülbírálja az előfizetés árazási rétegét.</span><span class="sxs-lookup"><span data-stu-id="b359a-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="b359a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="b359a-114">EXAMPLES</span></span>

### <span data-ttu-id="b359a-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b359a-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="b359a-116">Beilleszti az előfizetéshez tartozó összes beállított árazási szintet, valamint az alatta lévő erőforráscsoportokat.</span><span class="sxs-lookup"><span data-stu-id="b359a-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="b359a-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="b359a-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="b359a-118">Beolvassa a beállított árazási szintet a "myService1" erőforrás-gorup.</span><span class="sxs-lookup"><span data-stu-id="b359a-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="b359a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b359a-119">PARAMETERS</span></span>

### <span data-ttu-id="b359a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b359a-120">-DefaultProfile</span></span>
<span data-ttu-id="b359a-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b359a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b359a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b359a-122">-Name</span></span>
<span data-ttu-id="b359a-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b359a-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b359a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b359a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b359a-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b359a-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b359a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b359a-126">-ResourceId</span></span>
<span data-ttu-id="b359a-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b359a-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b359a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b359a-128">CommonParameters</span></span>
<span data-ttu-id="b359a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b359a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b359a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b359a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b359a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b359a-131">INPUTS</span></span>

### <span data-ttu-id="b359a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b359a-132">System.String</span></span>

## <span data-ttu-id="b359a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b359a-133">OUTPUTS</span></span>

### <span data-ttu-id="b359a-134">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b359a-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="b359a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b359a-135">NOTES</span></span>

## <span data-ttu-id="b359a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b359a-136">RELATED LINKS</span></span>
