---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010822"
---
# <span data-ttu-id="64163-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64163-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="64163-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64163-102">SYNOPSIS</span></span>
<span data-ttu-id="64163-103">HTTP-figyelőt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="64163-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="64163-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64163-104">SYNTAX</span></span>

### <span data-ttu-id="64163-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64163-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64163-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="64163-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64163-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="64163-107">DESCRIPTION</span></span>
<span data-ttu-id="64163-108">Az **Add-AzApplicationGatewayHttpListener** PARANCSMAG egy http-figyelőt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="64163-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="64163-109">Példák</span><span class="sxs-lookup"><span data-stu-id="64163-109">EXAMPLES</span></span>

### <span data-ttu-id="64163-110">1. példa: HTTP-figyelő felvétele</span><span class="sxs-lookup"><span data-stu-id="64163-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="64163-111">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs hozzáadja a HTTP-figyelőt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="64163-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="64163-112">2. példa: HTTPS-figyelő felvétele SSL-lel</span><span class="sxs-lookup"><span data-stu-id="64163-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="64163-113">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="64163-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="64163-114">A második parancs hozzáadja azt a figyelőt, amely a HTTPS protokollt használja az Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="64163-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="64163-115">3. példa: HTTPS-figyelő felvétele SSL-és állomásnevek használatával</span><span class="sxs-lookup"><span data-stu-id="64163-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="64163-116">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="64163-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="64163-117">A második parancs hozzáadja a figyelőt, amely a HTTPS protokollt használja az SSL-tanúsítványokkal és-állomásnevek használatával az Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="64163-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="64163-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64163-118">PARAMETERS</span></span>

### <span data-ttu-id="64163-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64163-119">-ApplicationGateway</span></span>
<span data-ttu-id="64163-120">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag hozzáadja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="64163-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="64163-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="64163-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="64163-122">Az alkalmazás-átjáró ügyfél-hibája</span><span class="sxs-lookup"><span data-stu-id="64163-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="64163-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64163-123">-DefaultProfile</span></span>
<span data-ttu-id="64163-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64163-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64163-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="64163-125">-FirewallPolicy</span></span>
<span data-ttu-id="64163-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="64163-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="64163-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="64163-127">-FirewallPolicyId</span></span>
<span data-ttu-id="64163-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="64163-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="64163-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64163-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="64163-130">Az Application Gateway előtér IP-erőforrás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="64163-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="64163-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="64163-132">Az Application Gateway előtér IP-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="64163-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="64163-133">-FrontendPort</span></span>
<span data-ttu-id="64163-134">Az alkalmazás-átjáró előtér-port objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="64163-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="64163-135">-FrontendPortId</span></span>
<span data-ttu-id="64163-136">Az Application Gateway előtér-port AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="64163-137">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="64163-137">-HostName</span></span>
<span data-ttu-id="64163-138">Annak az állomásnak a neve, amelyhez a parancsmag hozzáadja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="64163-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="64163-139">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="64163-139">-HostNames</span></span>
<span data-ttu-id="64163-140">Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="64163-140">Host names</span></span>

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

### <span data-ttu-id="64163-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64163-141">-Name</span></span>
<span data-ttu-id="64163-142">A parancs által hozzáadott előtér-végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="64163-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="64163-143">-Protocol</span></span>
<span data-ttu-id="64163-144">A HTTP-figyelő protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="64163-145">A HTTP és a HTTPS egyaránt támogatott.</span><span class="sxs-lookup"><span data-stu-id="64163-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="64163-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="64163-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="64163-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="64163-147">-SslCertificate</span></span>
<span data-ttu-id="64163-148">A HTTP-figyelő SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="64163-149">Meg kell adni, ha a HTTPS a figyelő protokollként van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="64163-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="64163-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="64163-150">-SslCertificateId</span></span>
<span data-ttu-id="64163-151">A HTTP-figyelő SSL-tanúsítványának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64163-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="64163-152">Meg kell adni, ha a HTTPS a figyelő protokollként van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="64163-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="64163-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64163-153">CommonParameters</span></span>
<span data-ttu-id="64163-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64163-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64163-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64163-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64163-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64163-156">INPUTS</span></span>

### <span data-ttu-id="64163-157">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64163-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="64163-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64163-158">OUTPUTS</span></span>

### <span data-ttu-id="64163-159">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64163-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="64163-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64163-160">NOTES</span></span>

## <span data-ttu-id="64163-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64163-161">RELATED LINKS</span></span>

[<span data-ttu-id="64163-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64163-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="64163-163">Új – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64163-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="64163-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64163-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="64163-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64163-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


