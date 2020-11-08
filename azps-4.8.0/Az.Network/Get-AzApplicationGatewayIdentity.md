---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182508"
---
# <span data-ttu-id="b1217-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="b1217-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="b1217-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1217-102">SYNOPSIS</span></span>
<span data-ttu-id="b1217-103">Az alkalmazás-átjáróhoz rendelt identitás beolvasása</span><span class="sxs-lookup"><span data-stu-id="b1217-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="b1217-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1217-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1217-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1217-105">DESCRIPTION</span></span>
<span data-ttu-id="b1217-106">A **Get-AzApplicationGatewayIdentity** parancsmag az alkalmazás-átjáróhoz rendelt identitást kapja.</span><span class="sxs-lookup"><span data-stu-id="b1217-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="b1217-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1217-107">EXAMPLES</span></span>

### <span data-ttu-id="b1217-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b1217-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="b1217-109">Ez a példa azt mutatja be, hogy miként szerezheti be az alkalmazásobjektum-identitást az alkalmazás-Átjáróból.</span><span class="sxs-lookup"><span data-stu-id="b1217-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="b1217-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1217-110">PARAMETERS</span></span>

### <span data-ttu-id="b1217-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1217-111">-ApplicationGateway</span></span>
<span data-ttu-id="b1217-112">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1217-112">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1217-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1217-113">-DefaultProfile</span></span>
<span data-ttu-id="b1217-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1217-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1217-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1217-115">CommonParameters</span></span>
<span data-ttu-id="b1217-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1217-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1217-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b1217-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1217-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1217-118">INPUTS</span></span>

### <span data-ttu-id="b1217-119">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1217-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1217-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1217-120">OUTPUTS</span></span>

### <span data-ttu-id="b1217-121">Microsoft. Azure. commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b1217-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="b1217-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1217-122">NOTES</span></span>

## <span data-ttu-id="b1217-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1217-123">RELATED LINKS</span></span>
