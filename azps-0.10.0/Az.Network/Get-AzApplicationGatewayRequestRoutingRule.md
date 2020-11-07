---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 402084acc332102c8a2f003e31e140b175b6f22f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841721"
---
# <span data-ttu-id="34dab-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34dab-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="34dab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34dab-102">SYNOPSIS</span></span>
<span data-ttu-id="34dab-103">Az alkalmazás-átjáró kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="34dab-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="34dab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34dab-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34dab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34dab-105">DESCRIPTION</span></span>
<span data-ttu-id="34dab-106">A **Get-AzApplicationGatewayRequestRoutingRule** parancsmag az alkalmazás-átjárók kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="34dab-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="34dab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="34dab-107">EXAMPLES</span></span>

### <span data-ttu-id="34dab-108">Példa 1: adott kérés útválasztási szabályának beszerzése</span><span class="sxs-lookup"><span data-stu-id="34dab-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="34dab-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="34dab-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="34dab-110">A második parancs a Rule01 nevű útválasztási szabályt a $AppGW nevű változóban tárolt alkalmazás-átjáróról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="34dab-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="34dab-111">2. példa: a kérési útválasztási szabályok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="34dab-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="34dab-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="34dab-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="34dab-113">A második parancs a $AppGW nevű változóban tárolt alkalmazás-útválasztási szabályok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="34dab-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="34dab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34dab-114">PARAMETERS</span></span>

### <span data-ttu-id="34dab-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34dab-115">-ApplicationGateway</span></span>
<span data-ttu-id="34dab-116">A kérés útválasztási szabályát tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="34dab-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="34dab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34dab-117">-DefaultProfile</span></span>
<span data-ttu-id="34dab-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34dab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34dab-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34dab-119">-Name</span></span>
<span data-ttu-id="34dab-120">Annak a kérési művelettervi szabálynak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="34dab-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="34dab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34dab-121">CommonParameters</span></span>
<span data-ttu-id="34dab-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34dab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34dab-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34dab-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34dab-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34dab-124">INPUTS</span></span>

### <span data-ttu-id="34dab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="34dab-125">System.String</span></span>

## <span data-ttu-id="34dab-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34dab-126">OUTPUTS</span></span>

### <span data-ttu-id="34dab-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34dab-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="34dab-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34dab-128">NOTES</span></span>

## <span data-ttu-id="34dab-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34dab-129">RELATED LINKS</span></span>

[<span data-ttu-id="34dab-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34dab-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="34dab-131">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34dab-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="34dab-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34dab-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="34dab-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34dab-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


