---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: fb171429e6b704964e0bbff68d301cc5f712c185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493091"
---
# <span data-ttu-id="c8419-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8419-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c8419-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8419-102">SYNOPSIS</span></span>
<span data-ttu-id="c8419-103">Módosítja a kérések útválasztási szabályát egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c8419-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8419-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8419-104">SYNTAX</span></span>

### <span data-ttu-id="c8419-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c8419-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8419-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c8419-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8419-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8419-107">DESCRIPTION</span></span>
<span data-ttu-id="c8419-108">A **set-AzureRmApplicationGatewayRequestRoutingRule** parancsmag módosítja a kérések útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="c8419-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="c8419-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c8419-109">EXAMPLES</span></span>

### <span data-ttu-id="c8419-110">Példa 1: a Request útválasztási szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="c8419-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c8419-111">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c8419-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c8419-112">A második parancs módosítja az alkalmazás átjárójának Request (útválasztási) szabályát a $Setting változóban megadott, a $Listener változóban megadott HTTP-figyelők, valamint a $Pool változóban megadott, a végpontokat tartalmazó címkészlet használatára.</span><span class="sxs-lookup"><span data-stu-id="c8419-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="c8419-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8419-113">PARAMETERS</span></span>

### <span data-ttu-id="c8419-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8419-114">-ApplicationGateway</span></span>
<span data-ttu-id="c8419-115">Azt az alkalmazásobjektum-objektumot adja meg, amelyhez ez a parancsmag a kérések útválasztási szabályát társítja.</span><span class="sxs-lookup"><span data-stu-id="c8419-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="c8419-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c8419-116">-BackendAddressPool</span></span>
<span data-ttu-id="c8419-117">Az Application Gateway back-end címkészletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8419-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c8419-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c8419-119">Az Application Gateway back-end Address Pool AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8419-119">Specifies the application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c8419-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c8419-121">Az Application Gateway backend HTTP-beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8419-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c8419-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c8419-123">Az Application Gateway back-end HTTP-beállításai AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8419-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8419-124">-DefaultProfile</span></span>
<span data-ttu-id="c8419-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8419-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8419-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c8419-126">-HttpListener</span></span>
<span data-ttu-id="c8419-127">Az Application Gateway HTTP-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8419-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="c8419-128">-HttpListenerId</span></span>
<span data-ttu-id="c8419-129">Az alkalmazás-átjáró HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8419-129">Specifies the application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8419-130">-Name</span></span>
<span data-ttu-id="c8419-131">Annak a kérési művelettervi szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="c8419-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c8419-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8419-132">-RedirectConfiguration</span></span>
<span data-ttu-id="c8419-133">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8419-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c8419-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="c8419-135">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="c8419-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c8419-136">-RuleType</span></span>
<span data-ttu-id="c8419-137">A Request útválasztási szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8419-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c8419-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="c8419-139">-UrlPathMapId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8419-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8419-140">CommonParameters</span></span>
<span data-ttu-id="c8419-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8419-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8419-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8419-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8419-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8419-143">INPUTS</span></span>

### <span data-ttu-id="c8419-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c8419-144">System.String</span></span>

## <span data-ttu-id="c8419-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8419-145">OUTPUTS</span></span>

### <span data-ttu-id="c8419-146">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8419-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8419-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8419-147">NOTES</span></span>

## <span data-ttu-id="c8419-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8419-148">RELATED LINKS</span></span>

[<span data-ttu-id="c8419-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8419-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c8419-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8419-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c8419-151">Új – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8419-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c8419-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8419-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


