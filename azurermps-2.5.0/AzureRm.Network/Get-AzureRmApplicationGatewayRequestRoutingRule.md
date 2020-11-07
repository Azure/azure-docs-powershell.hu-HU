---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: de019ffd1bc3be0e66cef6e8a15912f18b05f770
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850741"
---
# <span data-ttu-id="86b4a-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86b4a-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="86b4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="86b4a-103">Az alkalmazás-átjáró kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="86b4a-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86b4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86b4a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86b4a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="86b4a-106">A **Get-AzureRmApplicationGatewayRequestRoutingRule** parancsmag az alkalmazás-átjárók kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="86b4a-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="86b4a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86b4a-107">EXAMPLES</span></span>

### <span data-ttu-id="86b4a-108">Példa 1: adott kérés útválasztási szabályának beszerzése</span><span class="sxs-lookup"><span data-stu-id="86b4a-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="86b4a-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="86b4a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="86b4a-110">A második parancs a Rule01 nevű útválasztási szabályt a $AppGW nevű változóban tárolt alkalmazás-átjáróról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86b4a-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="86b4a-111">2. példa: a kérési útválasztási szabályok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="86b4a-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="86b4a-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="86b4a-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="86b4a-113">A második parancs a $AppGW nevű változóban tárolt alkalmazás-útválasztási szabályok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86b4a-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="86b4a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86b4a-114">PARAMETERS</span></span>

### <span data-ttu-id="86b4a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86b4a-115">-ApplicationGateway</span></span>
<span data-ttu-id="86b4a-116">A kérés útválasztási szabályát tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="86b4a-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="86b4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b4a-117">-DefaultProfile</span></span>
<span data-ttu-id="86b4a-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86b4a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86b4a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86b4a-119">-Name</span></span>
<span data-ttu-id="86b4a-120">Annak a kérési művelettervi szabálynak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="86b4a-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="86b4a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b4a-121">CommonParameters</span></span>
<span data-ttu-id="86b4a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86b4a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b4a-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b4a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b4a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86b4a-124">INPUTS</span></span>

### <span data-ttu-id="86b4a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="86b4a-125">System.String</span></span>

## <span data-ttu-id="86b4a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86b4a-126">OUTPUTS</span></span>

### <span data-ttu-id="86b4a-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86b4a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="86b4a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86b4a-128">NOTES</span></span>

## <span data-ttu-id="86b4a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86b4a-129">RELATED LINKS</span></span>

[<span data-ttu-id="86b4a-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86b4a-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="86b4a-131">Új – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86b4a-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="86b4a-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86b4a-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="86b4a-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86b4a-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


