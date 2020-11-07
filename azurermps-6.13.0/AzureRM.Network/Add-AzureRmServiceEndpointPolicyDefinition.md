---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679539"
---
# <span data-ttu-id="10212-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="10212-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="10212-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10212-102">SYNOPSIS</span></span>
<span data-ttu-id="10212-103">A szolgáltatás végpont-házirendjének definícióját hozzáadja egy adott házirendhez.</span><span class="sxs-lookup"><span data-stu-id="10212-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10212-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10212-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10212-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10212-105">DESCRIPTION</span></span>
<span data-ttu-id="10212-106">A **Add-AzureRmServiceEndpointPolicyDefinition** parancsmag szolgáltatási végpont házirend-definícióját adja hozzá a házirendhez.</span><span class="sxs-lookup"><span data-stu-id="10212-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="10212-107">Példák</span><span class="sxs-lookup"><span data-stu-id="10212-107">EXAMPLES</span></span>

### <span data-ttu-id="10212-108">1. példa: a szolgáltatás végpont-házirendjének definícióját frissíti egy szolgáltatási végpont-házirendben</span><span class="sxs-lookup"><span data-stu-id="10212-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="10212-109">Ez a parancs frissítette a szolgáltatás végpontjának házirend-definícióját a name ServiceEndpointPolicyDefinition1, a Service Microsoft. Storage, a Service Resources-előfizetés/sub1 és a Description (új definíció) című témakörben, amely a ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $policydef változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="10212-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="10212-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10212-110">PARAMETERS</span></span>

### <span data-ttu-id="10212-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10212-111">-DefaultProfile</span></span>
<span data-ttu-id="10212-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10212-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10212-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="10212-113">-Description</span></span>
<span data-ttu-id="10212-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="10212-114">The description of the definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10212-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10212-115">-Name</span></span>
<span data-ttu-id="10212-116">A szolgáltatás végpontjának házirend-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="10212-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="10212-117">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="10212-117">-Service</span></span>
<span data-ttu-id="10212-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="10212-118">Name of the service</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10212-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="10212-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="10212-120">A ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="10212-120">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10212-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="10212-121">-ServiceResource</span></span>
<span data-ttu-id="10212-122">A szolgáltatási erőforrások listája</span><span class="sxs-lookup"><span data-stu-id="10212-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10212-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10212-123">CommonParameters</span></span>
<span data-ttu-id="10212-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10212-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="10212-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10212-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10212-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10212-126">INPUTS</span></span>

### <span data-ttu-id="10212-127">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="10212-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="10212-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10212-128">OUTPUTS</span></span>

### <span data-ttu-id="10212-129">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="10212-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="10212-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10212-130">NOTES</span></span>

## <span data-ttu-id="10212-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10212-131">RELATED LINKS</span></span>
