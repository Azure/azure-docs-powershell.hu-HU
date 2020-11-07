---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: c138ced515932d158bb2a4a067ed405d8084db4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849226"
---
# <span data-ttu-id="6d3fe-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6d3fe-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="6d3fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3fe-103">Beilleszti az alkalmazás átjárójának előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6d3fe-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d3fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d3fe-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d3fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d3fe-105">DESCRIPTION</span></span>
<span data-ttu-id="6d3fe-106">A **Get-AzureRmApplicationGatewayFrontendIPConfig** parancsmag az alkalmazás-átjárók ELŐTÉR IP-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6d3fe-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="6d3fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6d3fe-107">EXAMPLES</span></span>

### <span data-ttu-id="6d3fe-108">Példa 1: meghatározott előtér-IP-konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d3fe-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="6d3fe-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja. A második parancs beilleszti a FrontEndIP01 nevű előtér IP-konfigurációját a $AppGw, és a $FrontEndIP változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6d3fe-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="6d3fe-110">2. példa: az előtér-IP-konfigurációk listáját tartalmazó lista beszerzése</span><span class="sxs-lookup"><span data-stu-id="6d3fe-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="6d3fe-111">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót a ResourceGroup01 nevű erőforráscsoport nevéből, és a $AppGw változóban tárolja. A második parancs beolvassa a $AppGwból az előtér IP-konfigurációjának listáját, és a $FrontEndIPs változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6d3fe-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="6d3fe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d3fe-112">PARAMETERS</span></span>

### <span data-ttu-id="6d3fe-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d3fe-113">-ApplicationGateway</span></span>
<span data-ttu-id="6d3fe-114">Azt az Application Gateway-objektumot adja meg, amely az előtér IP-konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6d3fe-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="6d3fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3fe-115">-DefaultProfile</span></span>
<span data-ttu-id="6d3fe-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d3fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d3fe-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d3fe-117">-Name</span></span>
<span data-ttu-id="6d3fe-118">Annak az előtér-IP-konfigurációnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="6d3fe-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6d3fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3fe-119">CommonParameters</span></span>
<span data-ttu-id="6d3fe-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d3fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3fe-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3fe-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d3fe-122">INPUTS</span></span>

### <span data-ttu-id="6d3fe-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6d3fe-123">System.String</span></span>

## <span data-ttu-id="6d3fe-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d3fe-124">OUTPUTS</span></span>

### <span data-ttu-id="6d3fe-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d3fe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="6d3fe-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d3fe-126">NOTES</span></span>

## <span data-ttu-id="6d3fe-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d3fe-127">RELATED LINKS</span></span>

[<span data-ttu-id="6d3fe-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6d3fe-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6d3fe-129">Új – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6d3fe-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6d3fe-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6d3fe-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="6d3fe-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6d3fe-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


