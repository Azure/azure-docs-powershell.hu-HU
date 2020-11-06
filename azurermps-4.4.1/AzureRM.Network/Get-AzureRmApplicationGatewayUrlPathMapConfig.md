---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 4a15bf67906606735b47e48b62d3e35cbcc91914
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492476"
---
# <span data-ttu-id="c2794-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2794-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="c2794-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2794-102">SYNOPSIS</span></span>
<span data-ttu-id="c2794-103">URL-elérésiút-megfeleltetések tömbje egy backend-kiszolgáló készletéből.</span><span class="sxs-lookup"><span data-stu-id="c2794-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2794-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2794-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2794-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2794-105">DESCRIPTION</span></span>
<span data-ttu-id="c2794-106">A **Get-AzureRmApplicationGatewayURLPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést kap a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="c2794-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c2794-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c2794-107">EXAMPLES</span></span>

### <span data-ttu-id="c2794-108">Példa 1: URL-elérési út megfeleltetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="c2794-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="c2794-109">Ez a parancs beolvassa az URL Path Map-konfigurációt az átjáró nevű alkalmazás-átjáróban található backend-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="c2794-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="c2794-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2794-110">PARAMETERS</span></span>

### <span data-ttu-id="c2794-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2794-111">-ApplicationGateway</span></span>
<span data-ttu-id="c2794-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérési út megfeleltetését kapja.</span><span class="sxs-lookup"><span data-stu-id="c2794-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="c2794-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2794-113">-Name</span></span>
<span data-ttu-id="c2794-114">Annak az URL-címnek a nevét adja meg, amelyben ez a parancsmag a Path Map konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="c2794-114">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="c2794-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2794-115">-DefaultProfile</span></span>
<span data-ttu-id="c2794-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2794-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2794-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2794-117">CommonParameters</span></span>
<span data-ttu-id="c2794-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2794-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2794-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2794-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2794-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2794-120">INPUTS</span></span>

### <span data-ttu-id="c2794-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2794-121">PSApplicationGateway</span></span>
<span data-ttu-id="c2794-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c2794-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="c2794-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2794-123">OUTPUTS</span></span>

### <span data-ttu-id="c2794-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c2794-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="c2794-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="c2794-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="c2794-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2794-126">NOTES</span></span>

## <span data-ttu-id="c2794-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2794-127">RELATED LINKS</span></span>

[<span data-ttu-id="c2794-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2794-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2794-129">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2794-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2794-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2794-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2794-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2794-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


