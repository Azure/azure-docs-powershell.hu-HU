---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ac85a308b73d822846a2f2a0a7b9ddf9ccc05cbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837367"
---
# <span data-ttu-id="04c3c-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04c3c-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="04c3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="04c3c-103">URL-elérésiút-megfeleltetések tömbje egy backend-kiszolgáló készletéből.</span><span class="sxs-lookup"><span data-stu-id="04c3c-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="04c3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04c3c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c3c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="04c3c-106">A **Get-AzApplicationGatewayURLPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést kap a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="04c3c-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="04c3c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="04c3c-108">Példa 1: URL-elérési út megfeleltetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="04c3c-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="04c3c-109">Ez a parancs beolvassa az URL Path Map-konfigurációt az átjáró nevű alkalmazás-átjáróban található backend-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="04c3c-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="04c3c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04c3c-110">PARAMETERS</span></span>

### <span data-ttu-id="04c3c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04c3c-111">-ApplicationGateway</span></span>
<span data-ttu-id="04c3c-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérési út megfeleltetését kapja.</span><span class="sxs-lookup"><span data-stu-id="04c3c-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="04c3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c3c-113">-DefaultProfile</span></span>
<span data-ttu-id="04c3c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04c3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04c3c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04c3c-115">-Name</span></span>
<span data-ttu-id="04c3c-116">Annak az URL-címnek a nevét adja meg, amelyben ez a parancsmag a Path Map konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="04c3c-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="04c3c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c3c-117">CommonParameters</span></span>
<span data-ttu-id="04c3c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04c3c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c3c-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="04c3c-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c3c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04c3c-120">INPUTS</span></span>

### <span data-ttu-id="04c3c-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04c3c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04c3c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04c3c-122">OUTPUTS</span></span>

### <span data-ttu-id="04c3c-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="04c3c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="04c3c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04c3c-124">NOTES</span></span>

## <span data-ttu-id="04c3c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04c3c-125">RELATED LINKS</span></span>

[<span data-ttu-id="04c3c-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04c3c-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="04c3c-127">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04c3c-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="04c3c-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04c3c-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="04c3c-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04c3c-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


