---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 564c586218297b8a22f0763a6747b6b451018a5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493445"
---
# <span data-ttu-id="841bd-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="841bd-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="841bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="841bd-102">SYNOPSIS</span></span>
<span data-ttu-id="841bd-103">Beolvassa az alkalmazás átjárójának HTTP-figyelését.</span><span class="sxs-lookup"><span data-stu-id="841bd-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="841bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="841bd-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="841bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="841bd-105">DESCRIPTION</span></span>
<span data-ttu-id="841bd-106">A **Get-AzureRmApplicationGatewayHttpListener** parancsmag az alkalmazás-ÁTJÁRÓk http-figyelését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="841bd-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="841bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="841bd-107">EXAMPLES</span></span>

### <span data-ttu-id="841bd-108">Példa 1: speciális HTTP-figyelő beszerzése</span><span class="sxs-lookup"><span data-stu-id="841bd-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="841bd-109">Ez a parancs a Listener01 nevű HTTP-figyelőt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="841bd-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="841bd-110">2. példa: a HTTP-figyelők listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="841bd-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="841bd-111">Ez a parancs a HTTP-figyelők listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="841bd-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="841bd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="841bd-112">PARAMETERS</span></span>

### <span data-ttu-id="841bd-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="841bd-113">-ApplicationGateway</span></span>
<span data-ttu-id="841bd-114">A HTTP-figyelőt tartalmazó Application Gateway-objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="841bd-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="841bd-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="841bd-115">-Name</span></span>
<span data-ttu-id="841bd-116">Annak a HTTP-figyelőnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="841bd-116">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="841bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841bd-117">-DefaultProfile</span></span>
<span data-ttu-id="841bd-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="841bd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="841bd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841bd-119">CommonParameters</span></span>
<span data-ttu-id="841bd-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="841bd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841bd-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="841bd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841bd-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="841bd-122">INPUTS</span></span>

### <span data-ttu-id="841bd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="841bd-123">System.String</span></span>

## <span data-ttu-id="841bd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="841bd-124">OUTPUTS</span></span>

### <span data-ttu-id="841bd-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="841bd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="841bd-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="841bd-126">NOTES</span></span>

## <span data-ttu-id="841bd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="841bd-127">RELATED LINKS</span></span>

[<span data-ttu-id="841bd-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="841bd-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="841bd-129">Új – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="841bd-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="841bd-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="841bd-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="841bd-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="841bd-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


