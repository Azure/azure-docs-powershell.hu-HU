---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 46a6a9663e7e22fd1182656bab9cab8a263f6c44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673036"
---
# <span data-ttu-id="cdb86-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cdb86-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="cdb86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdb86-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb86-103">A kérések útválasztási szabályait hozzáadja az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cdb86-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdb86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdb86-104">SYNTAX</span></span>

### <span data-ttu-id="cdb86-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb86-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdb86-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cdb86-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdb86-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdb86-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb86-108">Az **Add-AzureRmApplicationGatewayRequestRoutingRule** parancsmag a kérések útválasztási szabályait hozzáadja egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cdb86-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="cdb86-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cdb86-109">EXAMPLES</span></span>

### <span data-ttu-id="cdb86-110">1. példa: kérés-útválasztási szabály hozzáadása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="cdb86-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="cdb86-111">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdb86-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cdb86-112">A második parancs hozzáadja a Request Routing szabályt az Application Gateway programhoz.</span><span class="sxs-lookup"><span data-stu-id="cdb86-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="cdb86-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdb86-113">PARAMETERS</span></span>

### <span data-ttu-id="cdb86-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdb86-114">-ApplicationGateway</span></span>
<span data-ttu-id="cdb86-115">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a kérések útválasztási szabályát felveszi.</span><span class="sxs-lookup"><span data-stu-id="cdb86-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="cdb86-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cdb86-116">-BackendAddressPool</span></span>
<span data-ttu-id="cdb86-117">Az Application Gateway back-end Address Pool objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdb86-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="cdb86-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="cdb86-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="cdb86-119">Az Application Gateway back-end Address Pool AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdb86-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="cdb86-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cdb86-120">-BackendHttpSettings</span></span>
<span data-ttu-id="cdb86-121">Egy alkalmazás átjárójának back-end HTTP Settings objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdb86-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="cdb86-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="cdb86-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="cdb86-123">A backend HTTP-beállítási AZONOSÍTÓját adja meg az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="cdb86-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="cdb86-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb86-124">-DefaultProfile</span></span>
<span data-ttu-id="cdb86-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdb86-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb86-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="cdb86-126">-HttpListener</span></span>
<span data-ttu-id="cdb86-127">Az Application Gateway HTTP-figyelő objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdb86-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="cdb86-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="cdb86-128">-HttpListenerId</span></span>
<span data-ttu-id="cdb86-129">Az Application Gateway HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdb86-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="cdb86-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdb86-130">-Name</span></span>
<span data-ttu-id="cdb86-131">A Request Routing szabály nevét adja meg, amely a parancsmagot adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="cdb86-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="cdb86-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdb86-132">-RedirectConfiguration</span></span>
<span data-ttu-id="cdb86-133">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdb86-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="cdb86-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cdb86-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="cdb86-135">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="cdb86-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="cdb86-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="cdb86-136">-RuleType</span></span>
<span data-ttu-id="cdb86-137">A Request útválasztási szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdb86-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="cdb86-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="cdb86-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="cdb86-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="cdb86-139">-UrlPathMapId</span></span>
<span data-ttu-id="cdb86-140">A művelettervi szabály URL-elérési útjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdb86-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="cdb86-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb86-141">CommonParameters</span></span>
<span data-ttu-id="cdb86-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdb86-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb86-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb86-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb86-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdb86-144">INPUTS</span></span>

### <span data-ttu-id="cdb86-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cdb86-145">System.String</span></span>

## <span data-ttu-id="cdb86-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdb86-146">OUTPUTS</span></span>

### <span data-ttu-id="cdb86-147">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdb86-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cdb86-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdb86-148">NOTES</span></span>

## <span data-ttu-id="cdb86-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdb86-149">RELATED LINKS</span></span>

[<span data-ttu-id="cdb86-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cdb86-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="cdb86-151">Új – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cdb86-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="cdb86-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cdb86-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="cdb86-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cdb86-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


