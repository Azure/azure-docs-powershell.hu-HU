---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503507"
---
# <span data-ttu-id="bc305-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bc305-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="bc305-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc305-102">SYNOPSIS</span></span>
<span data-ttu-id="bc305-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="bc305-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc305-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc305-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc305-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc305-105">DESCRIPTION</span></span>
<span data-ttu-id="bc305-106">A **Remove-AzureRmServiceEndpointPolicy** parancsmag eltávolítja a szolgáltatási végpontok házirendjét.</span><span class="sxs-lookup"><span data-stu-id="bc305-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="bc305-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc305-107">EXAMPLES</span></span>

### <span data-ttu-id="bc305-108">1. példa: a szolgáltatás végpont-házirendjének eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="bc305-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="bc305-109">Ez a parancs eltávolítja a szolgáltatás végpontjának házirendjét a név PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="bc305-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="bc305-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc305-110">PARAMETERS</span></span>

### <span data-ttu-id="bc305-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc305-111">-DefaultProfile</span></span>
<span data-ttu-id="bc305-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc305-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc305-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc305-113">-Name</span></span>
<span data-ttu-id="bc305-114">A szolgáltatás végpont-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="bc305-114">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="bc305-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bc305-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="bc305-116">A ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bc305-116">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="bc305-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc305-117">CommonParameters</span></span>
<span data-ttu-id="bc305-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc305-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bc305-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc305-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc305-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc305-120">INPUTS</span></span>

### <span data-ttu-id="bc305-121">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bc305-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="bc305-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc305-122">OUTPUTS</span></span>

### <span data-ttu-id="bc305-123">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bc305-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="bc305-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc305-124">NOTES</span></span>

## <span data-ttu-id="bc305-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc305-125">RELATED LINKS</span></span>
