---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501999"
---
# <span data-ttu-id="6b6e6-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6b6e6-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="6b6e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6e6-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="6b6e6-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b6e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b6e6-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b6e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b6e6-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6e6-106">A **New-AzureRmServiceEndpointPolicyDefinition** parancsmag a szolgáltatás végpont-házirendjének definícióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="6b6e6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6b6e6-107">EXAMPLES</span></span>

### <span data-ttu-id="6b6e6-108">Példa 1: szolgáltatás végpont-házirendjének létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b6e6-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="6b6e6-109">Ez a parancs létrehozza a szolgáltatás végpontjának házirend-definícióját a name ServiceEndpointPolicyDefinition1, a Service Microsoft. Storage, a Service Resources-előfizetés/sub1 és a Description (új definíció) című témakörben, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $policydef változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="6b6e6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b6e6-110">PARAMETERS</span></span>

### <span data-ttu-id="6b6e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6e6-111">-DefaultProfile</span></span>
<span data-ttu-id="6b6e6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b6e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b6e6-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6b6e6-113">-Description</span></span>
<span data-ttu-id="6b6e6-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="6b6e6-114">The description of the definition</span></span>

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

### <span data-ttu-id="6b6e6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b6e6-115">-Name</span></span>
<span data-ttu-id="6b6e6-116">A szolgáltatás végpont-házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="6b6e6-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="6b6e6-117">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="6b6e6-117">-Service</span></span>
<span data-ttu-id="6b6e6-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="6b6e6-118">Name of the service</span></span>

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

### <span data-ttu-id="6b6e6-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="6b6e6-119">-ServiceResource</span></span>
<span data-ttu-id="6b6e6-120">A szolgáltatási erőforrások listája</span><span class="sxs-lookup"><span data-stu-id="6b6e6-120">List of service resources</span></span>

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

### <span data-ttu-id="6b6e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6e6-121">CommonParameters</span></span>
<span data-ttu-id="6b6e6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b6e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6b6e6-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6e6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6e6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b6e6-124">INPUTS</span></span>

### <span data-ttu-id="6b6e6-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b6e6-125">None</span></span>


## <span data-ttu-id="6b6e6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b6e6-126">OUTPUTS</span></span>

### <span data-ttu-id="6b6e6-127">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6b6e6-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="6b6e6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b6e6-128">NOTES</span></span>

## <span data-ttu-id="6b6e6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b6e6-129">RELATED LINKS</span></span>
