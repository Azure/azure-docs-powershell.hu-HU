---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501123"
---
# <span data-ttu-id="8ecfe-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ecfe-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8ecfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ecfe-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecfe-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="8ecfe-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ecfe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ecfe-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ecfe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ecfe-105">DESCRIPTION</span></span>
<span data-ttu-id="8ecfe-106">A **Get-AzureRmServiceEndpointPolicyDefinition** parancsmag szolgáltatási végpont házirend-definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="8ecfe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8ecfe-107">EXAMPLES</span></span>

### <span data-ttu-id="8ecfe-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8ecfe-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="8ecfe-109">Ez a parancs beolvassa a ServiceEndpointPolicyDefinition1-ban a ServiceEndpointPolicy $Policy nevű szolgáltatás végpont-házirendjének definícióját $policydef változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="8ecfe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ecfe-110">PARAMETERS</span></span>

### <span data-ttu-id="8ecfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecfe-111">-DefaultProfile</span></span>
<span data-ttu-id="8ecfe-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ecfe-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ecfe-113">-Name</span></span>
<span data-ttu-id="8ecfe-114">A szolgáltatás végpontjának házirend-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="8ecfe-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="8ecfe-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecfe-115">-ResourceId</span></span>
<span data-ttu-id="8ecfe-116">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="8ecfe-116">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="8ecfe-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecfe-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="8ecfe-118">A szolgáltatás végpontjának házirendje</span><span class="sxs-lookup"><span data-stu-id="8ecfe-118">The Service endpoint policy</span></span>

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

### <span data-ttu-id="8ecfe-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ecfe-119">-Confirm</span></span>
<span data-ttu-id="8ecfe-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ecfe-121">-WhatIf</span></span>
<span data-ttu-id="8ecfe-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ecfe-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ecfe-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecfe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecfe-124">CommonParameters</span></span>
<span data-ttu-id="8ecfe-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ecfe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecfe-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecfe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecfe-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ecfe-127">INPUTS</span></span>

### <span data-ttu-id="8ecfe-128">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecfe-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8ecfe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ecfe-129">OUTPUTS</span></span>

### <span data-ttu-id="8ecfe-130">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ecfe-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8ecfe-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ecfe-131">NOTES</span></span>

## <span data-ttu-id="8ecfe-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ecfe-132">RELATED LINKS</span></span>
