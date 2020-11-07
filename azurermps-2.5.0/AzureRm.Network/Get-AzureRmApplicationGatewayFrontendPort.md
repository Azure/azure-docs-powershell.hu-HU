---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: a8e6fffca256920f6d138088ef75ea6658ad1375
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849218"
---
# <span data-ttu-id="7cd23-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cd23-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7cd23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cd23-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd23-103">Beilleszti az alkalmazás átjárójának előtér-végpontját.</span><span class="sxs-lookup"><span data-stu-id="7cd23-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cd23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cd23-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cd23-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cd23-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd23-106">A **Get-AzureRmApplicationGatewayFrontendPort** parancsmag az alkalmazás-átjárók előtér-végpontját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7cd23-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="7cd23-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7cd23-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd23-108">Példa 1: meghatározott előtér-port beszerzése</span><span class="sxs-lookup"><span data-stu-id="7cd23-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7cd23-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7cd23-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7cd23-110">A második parancs a FrontEndPort01 nevű előtér-portot kapja $AppGw és a $FrontEndPort változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7cd23-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="7cd23-111">2. példa: az előtér-portok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="7cd23-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="7cd23-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7cd23-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7cd23-113">A második parancs beolvassa az előtér-portok listáját a $AppGwból, és a $FrontEndPorts változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7cd23-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="7cd23-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cd23-114">PARAMETERS</span></span>

### <span data-ttu-id="7cd23-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cd23-115">-ApplicationGateway</span></span>
<span data-ttu-id="7cd23-116">Megadja az előtér-portot tartalmazó Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="7cd23-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="7cd23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd23-117">-DefaultProfile</span></span>
<span data-ttu-id="7cd23-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cd23-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cd23-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cd23-119">-Name</span></span>
<span data-ttu-id="7cd23-120">A beolvasott előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cd23-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="7cd23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd23-121">CommonParameters</span></span>
<span data-ttu-id="7cd23-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cd23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd23-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd23-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd23-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cd23-124">INPUTS</span></span>

### <span data-ttu-id="7cd23-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd23-125">System.String</span></span>

## <span data-ttu-id="7cd23-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cd23-126">OUTPUTS</span></span>

### <span data-ttu-id="7cd23-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cd23-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7cd23-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cd23-128">NOTES</span></span>

## <span data-ttu-id="7cd23-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cd23-129">RELATED LINKS</span></span>

[<span data-ttu-id="7cd23-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cd23-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7cd23-131">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cd23-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7cd23-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cd23-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7cd23-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cd23-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


