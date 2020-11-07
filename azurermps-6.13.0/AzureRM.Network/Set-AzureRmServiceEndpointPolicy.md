---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672915"
---
# <span data-ttu-id="98ba8-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98ba8-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="98ba8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="98ba8-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="98ba8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98ba8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98ba8-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98ba8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="98ba8-106">A **set-AzureRmServiceEndpointPolicy** parancsmag szolgáltatás-végponti házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="98ba8-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="98ba8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="98ba8-108">1. példa: szolgáltatási végpontokra vonatkozó házirendet állít be</span><span class="sxs-lookup"><span data-stu-id="98ba8-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="98ba8-109">Ez a parancs frissíti az objektum által meghatározott Házirend1 nevű szolgáltatási végpont-házirendet, $serviceEndpointPolicy a "resourcegroup1" resourcegroup tartozik.</span><span class="sxs-lookup"><span data-stu-id="98ba8-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="98ba8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98ba8-110">PARAMETERS</span></span>

### <span data-ttu-id="98ba8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ba8-111">-DefaultProfile</span></span>
<span data-ttu-id="98ba8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98ba8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98ba8-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98ba8-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="98ba8-114">A ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98ba8-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="98ba8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ba8-115">CommonParameters</span></span>
<span data-ttu-id="98ba8-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98ba8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="98ba8-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98ba8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ba8-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98ba8-118">INPUTS</span></span>

### <span data-ttu-id="98ba8-119">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98ba8-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="98ba8-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98ba8-120">OUTPUTS</span></span>

### <span data-ttu-id="98ba8-121">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98ba8-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="98ba8-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98ba8-122">NOTES</span></span>

## <span data-ttu-id="98ba8-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98ba8-123">RELATED LINKS</span></span>
