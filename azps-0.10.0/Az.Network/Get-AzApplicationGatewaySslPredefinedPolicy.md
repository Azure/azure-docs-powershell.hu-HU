---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841689"
---
# <span data-ttu-id="594b7-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="594b7-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="594b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="594b7-102">SYNOPSIS</span></span>
<span data-ttu-id="594b7-103">Az alkalmazás-átjáró által megadott előre meghatározott SSL-házirendeket kapja.</span><span class="sxs-lookup"><span data-stu-id="594b7-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="594b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="594b7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="594b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="594b7-105">DESCRIPTION</span></span>
<span data-ttu-id="594b7-106">A **Get-AzApplicationGatewaySslPredefinedPolicy** parancsmag az Application Gateway által biztosított előre meghatározott SSL-házirendeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="594b7-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="594b7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="594b7-107">EXAMPLES</span></span>

### <span data-ttu-id="594b7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="594b7-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="594b7-109">Ez a parancs az összes előre definiált SSL-házirendet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="594b7-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="594b7-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="594b7-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="594b7-111">Ez a parancs előre definiált házirendet ad eredményül a name AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="594b7-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="594b7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="594b7-112">PARAMETERS</span></span>

### <span data-ttu-id="594b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594b7-113">-DefaultProfile</span></span>
<span data-ttu-id="594b7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="594b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="594b7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="594b7-115">-Name</span></span>
<span data-ttu-id="594b7-116">Az SSL-előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="594b7-116">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="594b7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594b7-117">CommonParameters</span></span>
<span data-ttu-id="594b7-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="594b7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594b7-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="594b7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594b7-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="594b7-120">INPUTS</span></span>

### <span data-ttu-id="594b7-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="594b7-121">None</span></span>

## <span data-ttu-id="594b7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="594b7-122">OUTPUTS</span></span>

### <span data-ttu-id="594b7-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="594b7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="594b7-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. commands. Network, Version = 4.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="594b7-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="594b7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="594b7-125">NOTES</span></span>

## <span data-ttu-id="594b7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="594b7-126">RELATED LINKS</span></span>

