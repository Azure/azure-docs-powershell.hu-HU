---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 03d47278681cbba23895c00b124cc3a2fc2cc6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680868"
---
# <span data-ttu-id="be9c9-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="be9c9-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="be9c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="be9c9-103">Az alkalmazás-átjáró által megadott előre meghatározott SSL-házirendeket kapja.</span><span class="sxs-lookup"><span data-stu-id="be9c9-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be9c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be9c9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be9c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="be9c9-106">A **Get-AzureRmApplicationGatewaySslPredefinedPolicy** parancsmag az Application Gateway által biztosított előre meghatározott SSL-házirendeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="be9c9-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="be9c9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="be9c9-107">EXAMPLES</span></span>

### <span data-ttu-id="be9c9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="be9c9-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="be9c9-109">Ez a parancs az összes előre definiált SSL-házirendet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="be9c9-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="be9c9-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="be9c9-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="be9c9-111">Ez a parancs előre definiált házirendet ad eredményül a name AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="be9c9-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="be9c9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be9c9-112">PARAMETERS</span></span>

### <span data-ttu-id="be9c9-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be9c9-113">-Name</span></span>
<span data-ttu-id="be9c9-114">Az SSL-előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="be9c9-114">Name of the ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be9c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be9c9-115">-DefaultProfile</span></span>
<span data-ttu-id="be9c9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be9c9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be9c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be9c9-117">CommonParameters</span></span>
<span data-ttu-id="be9c9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be9c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be9c9-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be9c9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be9c9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be9c9-120">INPUTS</span></span>

### <span data-ttu-id="be9c9-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="be9c9-121">None</span></span>

## <span data-ttu-id="be9c9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be9c9-122">OUTPUTS</span></span>

### <span data-ttu-id="be9c9-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="be9c9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="be9c9-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. commands. Network, Version = 4.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="be9c9-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="be9c9-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be9c9-125">NOTES</span></span>

## <span data-ttu-id="be9c9-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be9c9-126">RELATED LINKS</span></span>

