---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848737"
---
# <span data-ttu-id="36291-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36291-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="36291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36291-102">SYNOPSIS</span></span>
<span data-ttu-id="36291-103">Eltávolítja az URL-címek elérési útját a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="36291-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36291-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36291-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36291-105">DESCRIPTION</span></span>
<span data-ttu-id="36291-106">A **Remove-AzureRmApplicationGatewayUrlPathMapConfig** parancsmag eltávolítja az URL-elérési utakat a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="36291-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="36291-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36291-107">EXAMPLES</span></span>

### <span data-ttu-id="36291-108">1:</span><span class="sxs-lookup"><span data-stu-id="36291-108">1:</span></span>
```

```

## <span data-ttu-id="36291-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36291-109">PARAMETERS</span></span>

### <span data-ttu-id="36291-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36291-110">-ApplicationGateway</span></span>
<span data-ttu-id="36291-111">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja az URL Path Map-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="36291-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="36291-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36291-112">-DefaultProfile</span></span>
<span data-ttu-id="36291-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36291-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36291-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36291-114">-Name</span></span>
<span data-ttu-id="36291-115">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend-kiszolgálóról távolít el.</span><span class="sxs-lookup"><span data-stu-id="36291-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="36291-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36291-116">CommonParameters</span></span>
<span data-ttu-id="36291-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36291-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36291-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36291-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36291-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36291-119">INPUTS</span></span>

### <span data-ttu-id="36291-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36291-120">PSApplicationGateway</span></span>
<span data-ttu-id="36291-121">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="36291-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="36291-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36291-122">OUTPUTS</span></span>

### <span data-ttu-id="36291-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36291-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36291-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36291-124">NOTES</span></span>

## <span data-ttu-id="36291-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36291-125">RELATED LINKS</span></span>

[<span data-ttu-id="36291-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36291-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="36291-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36291-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="36291-128">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36291-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="36291-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="36291-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


