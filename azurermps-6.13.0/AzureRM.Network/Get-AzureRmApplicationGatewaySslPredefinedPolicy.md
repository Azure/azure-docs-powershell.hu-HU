---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 82713c41d6f2e3882c50ffbd5ab6b276a90dc2e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501140"
---
# <span data-ttu-id="b90fb-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="b90fb-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="b90fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b90fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b90fb-103">Az alkalmazás-átjáró által megadott előre meghatározott SSL-házirendeket kapja.</span><span class="sxs-lookup"><span data-stu-id="b90fb-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b90fb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b90fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b90fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b90fb-106">A **Get-AzureRmApplicationGatewaySslPredefinedPolicy** parancsmag az Application Gateway által biztosított előre meghatározott SSL-házirendeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b90fb-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="b90fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b90fb-107">EXAMPLES</span></span>

### <span data-ttu-id="b90fb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b90fb-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="b90fb-109">Ez a parancs az összes előre definiált SSL-házirendet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="b90fb-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="b90fb-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="b90fb-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="b90fb-111">Ez a parancs előre definiált házirendet ad eredményül a name AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="b90fb-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="b90fb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b90fb-112">PARAMETERS</span></span>

### <span data-ttu-id="b90fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90fb-113">-DefaultProfile</span></span>
<span data-ttu-id="b90fb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b90fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b90fb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b90fb-115">-Name</span></span>
<span data-ttu-id="b90fb-116">Az SSL-előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="b90fb-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="b90fb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90fb-117">CommonParameters</span></span>
<span data-ttu-id="b90fb-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b90fb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90fb-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90fb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90fb-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b90fb-120">INPUTS</span></span>

### <span data-ttu-id="b90fb-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="b90fb-121">None</span></span>

## <span data-ttu-id="b90fb-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b90fb-122">OUTPUTS</span></span>

### <span data-ttu-id="b90fb-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="b90fb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="b90fb-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b90fb-124">NOTES</span></span>

## <span data-ttu-id="b90fb-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b90fb-125">RELATED LINKS</span></span>
