---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494052"
---
# <span data-ttu-id="4184c-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4184c-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="4184c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4184c-102">SYNOPSIS</span></span>
<span data-ttu-id="4184c-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="4184c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4184c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4184c-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4184c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4184c-105">DESCRIPTION</span></span>
<span data-ttu-id="4184c-106">A **Get-AzureRmServiceEndpointPolicy** parancsmag szolgáltatási végpont-házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="4184c-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="4184c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4184c-107">EXAMPLES</span></span>

### <span data-ttu-id="4184c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4184c-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4184c-109">Ez a parancs a ServiceEndpointPolicy1 nevű, a ResourceGroup01 nevű erőforráscsoporthoz tartozó szolgáltatás-végponti házirendet kapja meg, és a $policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4184c-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="4184c-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="4184c-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4184c-111">Ez a parancs felsorolja a ResourceGroup01 nevű erőforráscsoport összes szolgáltatás-végpont-házirendjét, és a $policyList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4184c-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="4184c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4184c-112">PARAMETERS</span></span>

### <span data-ttu-id="4184c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4184c-113">-DefaultProfile</span></span>
<span data-ttu-id="4184c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4184c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4184c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4184c-115">-Name</span></span>
<span data-ttu-id="4184c-116">A szolgáltatás végpont-házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="4184c-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4184c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4184c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4184c-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4184c-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4184c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4184c-119">CommonParameters</span></span>
<span data-ttu-id="4184c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4184c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4184c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4184c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4184c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4184c-122">INPUTS</span></span>

### <span data-ttu-id="4184c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4184c-123">System.String</span></span>


## <span data-ttu-id="4184c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4184c-124">OUTPUTS</span></span>

### <span data-ttu-id="4184c-125">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4184c-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4184c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4184c-126">NOTES</span></span>

## <span data-ttu-id="4184c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4184c-127">RELATED LINKS</span></span>
