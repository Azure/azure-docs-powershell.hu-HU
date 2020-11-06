---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 612e6b0cb5438dbb37a2e9d1c77da151c852fac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495329"
---
# <span data-ttu-id="29166-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="29166-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="29166-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29166-102">SYNOPSIS</span></span>
<span data-ttu-id="29166-103">Eltávolítja az URL-címek elérési útját a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="29166-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29166-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29166-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29166-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29166-105">DESCRIPTION</span></span>
<span data-ttu-id="29166-106">A **Remove-AzureRmApplicationGatewayUrlPathMapConfig** parancsmag eltávolítja az URL-elérési utakat a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="29166-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="29166-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29166-107">EXAMPLES</span></span>

## <span data-ttu-id="29166-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29166-108">PARAMETERS</span></span>

### <span data-ttu-id="29166-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29166-109">-ApplicationGateway</span></span>
<span data-ttu-id="29166-110">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja az URL Path Map-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="29166-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29166-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29166-111">-DefaultProfile</span></span>
<span data-ttu-id="29166-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29166-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29166-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29166-113">-Name</span></span>
<span data-ttu-id="29166-114">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend-kiszolgálóról távolít el.</span><span class="sxs-lookup"><span data-stu-id="29166-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="29166-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29166-115">CommonParameters</span></span>
<span data-ttu-id="29166-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29166-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29166-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29166-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29166-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29166-118">INPUTS</span></span>

### <span data-ttu-id="29166-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29166-119">PSApplicationGateway</span></span>
<span data-ttu-id="29166-120">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="29166-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="29166-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29166-121">OUTPUTS</span></span>

### <span data-ttu-id="29166-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29166-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="29166-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29166-123">NOTES</span></span>

## <span data-ttu-id="29166-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29166-124">RELATED LINKS</span></span>

[<span data-ttu-id="29166-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="29166-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="29166-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="29166-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="29166-127">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="29166-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="29166-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="29166-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


