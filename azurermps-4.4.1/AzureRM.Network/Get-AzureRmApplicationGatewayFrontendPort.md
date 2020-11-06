---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: f0a897dfcc68d2313326d974d1b5a172bd79db6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493446"
---
# <span data-ttu-id="a2e46-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a2e46-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a2e46-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2e46-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e46-103">Beilleszti az alkalmazás átjárójának előtér-végpontját.</span><span class="sxs-lookup"><span data-stu-id="a2e46-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2e46-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2e46-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2e46-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2e46-105">DESCRIPTION</span></span>
<span data-ttu-id="a2e46-106">A **Get-AzureRmApplicationGatewayFrontendPort** parancsmag az alkalmazás-átjárók előtér-végpontját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2e46-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="a2e46-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2e46-107">EXAMPLES</span></span>

### <span data-ttu-id="a2e46-108">Példa 1: meghatározott előtér-port beszerzése</span><span class="sxs-lookup"><span data-stu-id="a2e46-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a2e46-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a2e46-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a2e46-110">A második parancs a FrontEndPort01 nevű előtér-portot kapja $AppGw és a $FrontEndPort változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a2e46-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="a2e46-111">2. példa: az előtér-portok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a2e46-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="a2e46-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a2e46-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a2e46-113">A második parancs beolvassa az előtér-portok listáját a $AppGwból, és a $FrontEndPorts változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a2e46-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="a2e46-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2e46-114">PARAMETERS</span></span>

### <span data-ttu-id="a2e46-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2e46-115">-ApplicationGateway</span></span>
<span data-ttu-id="a2e46-116">Megadja az előtér-portot tartalmazó Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="a2e46-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="a2e46-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2e46-117">-Name</span></span>
<span data-ttu-id="a2e46-118">A beolvasott előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2e46-118">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="a2e46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e46-119">-DefaultProfile</span></span>
<span data-ttu-id="a2e46-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2e46-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2e46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e46-121">CommonParameters</span></span>
<span data-ttu-id="a2e46-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2e46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e46-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e46-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e46-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e46-124">INPUTS</span></span>

### <span data-ttu-id="a2e46-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a2e46-125">System.String</span></span>

## <span data-ttu-id="a2e46-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e46-126">OUTPUTS</span></span>

### <span data-ttu-id="a2e46-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a2e46-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a2e46-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2e46-128">NOTES</span></span>

## <span data-ttu-id="a2e46-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2e46-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2e46-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a2e46-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a2e46-131">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a2e46-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a2e46-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a2e46-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a2e46-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a2e46-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


