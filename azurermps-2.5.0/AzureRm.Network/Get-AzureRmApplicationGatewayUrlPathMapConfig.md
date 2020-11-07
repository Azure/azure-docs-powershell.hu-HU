---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848465"
---
# <span data-ttu-id="7dc14-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7dc14-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7dc14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7dc14-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc14-103">URL-elérésiút-megfeleltetések tömbje egy backend-kiszolgáló készletéből.</span><span class="sxs-lookup"><span data-stu-id="7dc14-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7dc14-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dc14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7dc14-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc14-106">A **Get-AzureRmApplicationGatewayURLPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést kap a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="7dc14-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7dc14-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7dc14-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc14-108">Példa 1: URL-elérési út megfeleltetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="7dc14-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="7dc14-109">Ez a parancs beolvassa az URL Path Map-konfigurációt az átjáró nevű alkalmazás-átjáróban található backend-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="7dc14-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="7dc14-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7dc14-110">PARAMETERS</span></span>

### <span data-ttu-id="7dc14-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dc14-111">-ApplicationGateway</span></span>
<span data-ttu-id="7dc14-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérési út megfeleltetését kapja.</span><span class="sxs-lookup"><span data-stu-id="7dc14-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="7dc14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc14-113">-DefaultProfile</span></span>
<span data-ttu-id="7dc14-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7dc14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc14-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7dc14-115">-Name</span></span>
<span data-ttu-id="7dc14-116">Annak az URL-címnek a nevét adja meg, amelyben ez a parancsmag a Path Map konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="7dc14-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="7dc14-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc14-117">CommonParameters</span></span>
<span data-ttu-id="7dc14-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7dc14-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc14-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc14-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc14-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dc14-120">INPUTS</span></span>

### <span data-ttu-id="7dc14-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dc14-121">PSApplicationGateway</span></span>
<span data-ttu-id="7dc14-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7dc14-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7dc14-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dc14-123">OUTPUTS</span></span>

### <span data-ttu-id="7dc14-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="7dc14-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="7dc14-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="7dc14-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="7dc14-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7dc14-126">NOTES</span></span>

## <span data-ttu-id="7dc14-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7dc14-127">RELATED LINKS</span></span>

[<span data-ttu-id="7dc14-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7dc14-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7dc14-129">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7dc14-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7dc14-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7dc14-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7dc14-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7dc14-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


