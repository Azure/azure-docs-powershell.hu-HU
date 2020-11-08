---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 3cc9af0865ca47099f5617cc1e94f3232ed9bdb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184330"
---
# <span data-ttu-id="b6171-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6171-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b6171-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6171-102">SYNOPSIS</span></span>
<span data-ttu-id="b6171-103">Az alkalmazás-átjárók HTTP-figyelését módosítja.</span><span class="sxs-lookup"><span data-stu-id="b6171-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="b6171-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6171-104">SYNTAX</span></span>

### <span data-ttu-id="b6171-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6171-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6171-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b6171-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6171-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6171-107">DESCRIPTION</span></span>
<span data-ttu-id="b6171-108">A **set-AzApplicationGatewayHttpListener** parancsmag módosította az Azure Application ÁTJÁRÓk http-figyelőjét.</span><span class="sxs-lookup"><span data-stu-id="b6171-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="b6171-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b6171-109">EXAMPLES</span></span>

### <span data-ttu-id="b6171-110">Példa 1: HTTP-figyelő beállítása</span><span class="sxs-lookup"><span data-stu-id="b6171-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="b6171-111">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b6171-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b6171-112">A második parancs az átjáróhoz tartozó HTTP-figyelőt állítja be a 80 $FIP-on tárolt, az előtér-konfigurációban lévő HTTP-protokollon keresztül.</span><span class="sxs-lookup"><span data-stu-id="b6171-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="b6171-113">2. példa: HTTPS-figyelő felvétele SSL-és állomásnevek használatával</span><span class="sxs-lookup"><span data-stu-id="b6171-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="b6171-114">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b6171-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b6171-115">A második parancs hozzáadja a figyelőt, amely a HTTPS protokollt használja az SSL-tanúsítványokkal és-állomásnevek használatával az Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="b6171-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="b6171-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6171-116">PARAMETERS</span></span>

### <span data-ttu-id="b6171-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6171-117">-ApplicationGateway</span></span>
<span data-ttu-id="b6171-118">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag társítja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="b6171-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="b6171-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6171-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b6171-120">Az alkalmazás-átjáró ügyfél-hibája</span><span class="sxs-lookup"><span data-stu-id="b6171-120">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6171-121">-DefaultProfile</span></span>
<span data-ttu-id="b6171-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6171-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6171-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b6171-123">-FirewallPolicy</span></span>
<span data-ttu-id="b6171-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b6171-124">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b6171-125">-FirewallPolicyId</span></span>
<span data-ttu-id="b6171-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b6171-126">FirewallPolicyId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6171-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b6171-128">Az alkalmazás-átjáró előtér IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6171-128">Specifies the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b6171-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b6171-130">Az alkalmazás-átjáró előtér-IP-címének AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6171-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b6171-131">-FrontendPort</span></span>
<span data-ttu-id="b6171-132">Az Application Gateway előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6171-132">Specifies the application gateway front-end port.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b6171-133">-FrontendPortId</span></span>
<span data-ttu-id="b6171-134">Az Application Gateway előtér-port AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6171-134">Specifies the application gateway front-end port ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-135">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="b6171-135">-HostName</span></span>
<span data-ttu-id="b6171-136">Azt az állomásnevet adja meg, amelyre a parancsmag a HTTP-figyelőt elküldi.</span><span class="sxs-lookup"><span data-stu-id="b6171-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="b6171-137">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="b6171-137">-HostNames</span></span>
<span data-ttu-id="b6171-138">Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="b6171-138">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6171-139">-Name</span></span>
<span data-ttu-id="b6171-140">A HTTP-figyelő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6171-140">Specifies the name of the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b6171-141">-Protocol</span></span>
<span data-ttu-id="b6171-142">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6171-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="b6171-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b6171-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6171-144">Http</span><span class="sxs-lookup"><span data-stu-id="b6171-144">Http</span></span>
- <span data-ttu-id="b6171-145">Https</span><span class="sxs-lookup"><span data-stu-id="b6171-145">Https</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b6171-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="b6171-147">Azt adja meg, hogy a parancsmagnak meg kell-e adni a kiszolgálónév jelzését.</span><span class="sxs-lookup"><span data-stu-id="b6171-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="b6171-148">A paraméter elfogadható értékei a következők: igaz vagy hamis.</span><span class="sxs-lookup"><span data-stu-id="b6171-148">The acceptable values for this parameter are: true or false.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6171-149">-SslCertificate</span></span>
<span data-ttu-id="b6171-150">A HTTP-figyelő SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6171-150">Specifies the SSL certificate of the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b6171-151">-SslCertificateId</span></span>
<span data-ttu-id="b6171-152">Megadja a HTTP-figyelő Secure Socket Layer (SSL) tanúsítvány-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="b6171-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6171-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6171-153">CommonParameters</span></span>
<span data-ttu-id="b6171-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6171-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6171-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6171-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6171-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6171-156">INPUTS</span></span>

### <span data-ttu-id="b6171-157">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6171-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6171-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6171-158">OUTPUTS</span></span>

### <span data-ttu-id="b6171-159">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6171-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6171-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6171-160">NOTES</span></span>

## <span data-ttu-id="b6171-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6171-161">RELATED LINKS</span></span>

[<span data-ttu-id="b6171-162">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6171-162">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6171-163">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6171-163">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6171-164">Új – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6171-164">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6171-165">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6171-165">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


