---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 68676c05757a58f2c1094e36338d17a52de6b040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493631"
---
# <span data-ttu-id="f4108-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4108-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f4108-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4108-102">SYNOPSIS</span></span>
<span data-ttu-id="f4108-103">Eltávolítja az URL-címek elérési útját a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="f4108-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4108-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4108-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4108-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4108-105">DESCRIPTION</span></span>
<span data-ttu-id="f4108-106">A **Remove-AzureRmApplicationGatewayUrlPathMapConfig** parancsmag eltávolítja az URL-elérési utakat a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="f4108-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f4108-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4108-107">EXAMPLES</span></span>

## <span data-ttu-id="f4108-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4108-108">PARAMETERS</span></span>

### <span data-ttu-id="f4108-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4108-109">-ApplicationGateway</span></span>
<span data-ttu-id="f4108-110">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja az URL Path Map-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f4108-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="f4108-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4108-111">-DefaultProfile</span></span>
<span data-ttu-id="f4108-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4108-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4108-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4108-113">-Name</span></span>
<span data-ttu-id="f4108-114">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend-kiszolgálóról távolít el.</span><span class="sxs-lookup"><span data-stu-id="f4108-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="f4108-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4108-115">CommonParameters</span></span>
<span data-ttu-id="f4108-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4108-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4108-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4108-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4108-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4108-118">INPUTS</span></span>

### <span data-ttu-id="f4108-119">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4108-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f4108-120">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4108-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f4108-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4108-121">OUTPUTS</span></span>

### <span data-ttu-id="f4108-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4108-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4108-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4108-123">NOTES</span></span>

## <span data-ttu-id="f4108-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4108-124">RELATED LINKS</span></span>

[<span data-ttu-id="f4108-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4108-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f4108-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4108-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f4108-127">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4108-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f4108-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4108-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


