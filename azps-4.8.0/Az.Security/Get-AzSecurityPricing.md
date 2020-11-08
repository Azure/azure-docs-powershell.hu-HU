---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: a1b07c5fb76d912ec117d42497f0d0b14bfb298c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172749"
---
# <span data-ttu-id="c6c1f-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c6c1f-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="c6c1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c1f-103">Az Azure Security Center díjszabási küszöbértékét kapja meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="c6c1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6c1f-104">SYNTAX</span></span>

### <span data-ttu-id="c6c1f-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6c1f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c1f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c6c1f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c1f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c1f-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6c1f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6c1f-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c1f-109">Az Azure biztonsági központ árképzési rétege hatóköre, ezzel a parancsmaggal megadhatja a beállított árképzési szinteket.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="c6c1f-110">Az előfizetés árazási szintje tartalmazza az összes erőforráscsoport-csoportot.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="c6c1f-111">Az erőforráscsoport árazási szintje felülbírálja az előfizetés árazási rétegét.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="c6c1f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c6c1f-112">EXAMPLES</span></span>

### <span data-ttu-id="c6c1f-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6c1f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
Id--/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines
--                                                                                                                             ----       -----------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServers
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServerVirtualMachin…
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults
```

<span data-ttu-id="c6c1f-114">Beilleszti az előfizetéshez tartozó összes beállított árazási szintet, valamint az alatta lévő erőforráscsoportokat.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="c6c1f-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="c6c1f-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="c6c1f-116">Az "myService1" erőforráscsoport konfigurált árazási rétegét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="c6c1f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6c1f-117">PARAMETERS</span></span>

### <span data-ttu-id="c6c1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c1f-118">-DefaultProfile</span></span>
<span data-ttu-id="c6c1f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c1f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6c1f-120">-Name</span></span>
<span data-ttu-id="c6c1f-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="c6c1f-121">Resource name.</span></span>

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

### <span data-ttu-id="c6c1f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c1f-122">-ResourceId</span></span>
<span data-ttu-id="c6c1f-123">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-123">Resource ID.</span></span>

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

### <span data-ttu-id="c6c1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c1f-124">CommonParameters</span></span>
<span data-ttu-id="c6c1f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6c1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c1f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6c1f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c1f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c1f-127">INPUTS</span></span>

### <span data-ttu-id="c6c1f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c6c1f-128">System.String</span></span>

## <span data-ttu-id="c6c1f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c1f-129">OUTPUTS</span></span>

### <span data-ttu-id="c6c1f-130">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c6c1f-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="c6c1f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6c1f-131">NOTES</span></span>

## <span data-ttu-id="c6c1f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6c1f-132">RELATED LINKS</span></span>
