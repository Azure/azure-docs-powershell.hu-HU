---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672914"
---
# <span data-ttu-id="0f742-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0f742-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="0f742-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f742-102">SYNOPSIS</span></span>
<span data-ttu-id="0f742-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="0f742-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f742-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f742-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f742-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f742-105">DESCRIPTION</span></span>
<span data-ttu-id="0f742-106">A **set-AzureRmServiceEndpointPolicyDefinition** parancsmag szolgáltatás-végponti házirend-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0f742-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="0f742-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f742-107">EXAMPLES</span></span>

### <span data-ttu-id="0f742-108">1. példa: a szolgáltatás végpont-házirendjének definícióját frissíti egy szolgáltatási végpont-házirendben</span><span class="sxs-lookup"><span data-stu-id="0f742-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="0f742-109">Ez a parancs frissíti az objektum $ServiceEndpointPolicy által definiált szolgáltatási végpont házirendben a Policydef1 nevű szolgáltatási végpont házirend-definícióját.</span><span class="sxs-lookup"><span data-stu-id="0f742-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="0f742-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f742-110">PARAMETERS</span></span>

### <span data-ttu-id="0f742-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f742-111">-DefaultProfile</span></span>
<span data-ttu-id="0f742-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f742-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f742-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0f742-113">-Description</span></span>
<span data-ttu-id="0f742-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="0f742-114">The description of the definition</span></span>

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

### <span data-ttu-id="0f742-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f742-115">-Name</span></span>
<span data-ttu-id="0f742-116">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="0f742-116">The name of the rule</span></span>

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

### <span data-ttu-id="0f742-117">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="0f742-117">-Service</span></span>
<span data-ttu-id="0f742-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="0f742-118">Name of the service</span></span>

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

### <span data-ttu-id="0f742-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0f742-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="0f742-120">A NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0f742-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="0f742-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="0f742-121">-ServiceResource</span></span>
<span data-ttu-id="0f742-122">A szolgáltatási erőforrások listája</span><span class="sxs-lookup"><span data-stu-id="0f742-122">List of service resources</span></span>

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

### <span data-ttu-id="0f742-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f742-123">CommonParameters</span></span>
<span data-ttu-id="0f742-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f742-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0f742-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f742-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f742-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f742-126">INPUTS</span></span>

### <span data-ttu-id="0f742-127">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0f742-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="0f742-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f742-128">OUTPUTS</span></span>

### <span data-ttu-id="0f742-129">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0f742-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="0f742-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f742-130">NOTES</span></span>

## <span data-ttu-id="0f742-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f742-131">RELATED LINKS</span></span>
