---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: f769eb91d524bc9115199127833471246f6fdd1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157235"
---
# <span data-ttu-id="3f68a-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f68a-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3f68a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f68a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f68a-103">HTTP- hallgatót ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3f68a-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="3f68a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f68a-104">SYNTAX</span></span>

### <span data-ttu-id="3f68a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f68a-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f68a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3f68a-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f68a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f68a-107">DESCRIPTION</span></span>
<span data-ttu-id="3f68a-108">Az **Add-AzApplicationGatewayHttpListener parancsmag** hozzáad egy HTTP-hallgatót egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3f68a-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="3f68a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f68a-109">EXAMPLES</span></span>

### <span data-ttu-id="3f68a-110">1. példa: HTTP-hallgató hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3f68a-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="3f68a-111">Az első parancs az alkalmazás átjáróját a $AppGw tárolja. A második parancs hozzáadja a HTTP-hallgatót az alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3f68a-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="3f68a-112">2. példa: HTTPS-hallgató hozzáadása SSL-sel</span><span class="sxs-lookup"><span data-stu-id="3f68a-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="3f68a-113">Az első parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="3f68a-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3f68a-114">A második parancs hozzáadja a hallgatót, amely a HTTPS protokollt használja az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3f68a-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="3f68a-115">3. példa: HTTPS-hallgató hozzáadása SSL és HostNames szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="3f68a-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="3f68a-116">Az első parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="3f68a-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3f68a-117">A második parancs hozzáadja a hallgatót, amely a HTTPS protokollt használja SSL-tanúsítványokkal és HostNames-ekkel együtt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3f68a-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="3f68a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f68a-118">PARAMETERS</span></span>

### <span data-ttu-id="3f68a-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f68a-119">-ApplicationGateway</span></span>
<span data-ttu-id="3f68a-120">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag hozzáad egy HTTP-hallgatót.</span><span class="sxs-lookup"><span data-stu-id="3f68a-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="3f68a-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f68a-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="3f68a-122">Ügyfélhiba egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="3f68a-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="3f68a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f68a-123">-DefaultProfile</span></span>
<span data-ttu-id="3f68a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f68a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f68a-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3f68a-125">-FirewallPolicy</span></span>
<span data-ttu-id="3f68a-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3f68a-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="3f68a-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="3f68a-127">-FirewallPolicyId</span></span>
<span data-ttu-id="3f68a-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="3f68a-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="3f68a-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f68a-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="3f68a-130">Az alkalmazás átjárója előlapi IP-erőforrás-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f68a-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="3f68a-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3f68a-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="3f68a-132">Az alkalmazás átjárójának előlapi IP-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3f68a-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="3f68a-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3f68a-133">-FrontendPort</span></span>
<span data-ttu-id="3f68a-134">Az alkalmazás átjárójának előlapi portobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f68a-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="3f68a-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="3f68a-135">-FrontendPortId</span></span>
<span data-ttu-id="3f68a-136">Az alkalmazás átjárójának előlapi portazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f68a-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="3f68a-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="3f68a-137">-HostName</span></span>
<span data-ttu-id="3f68a-138">Megadja azt az állomásnevet, amelybe ez a parancsmag hozzáad egy HTTP-hallgatót.</span><span class="sxs-lookup"><span data-stu-id="3f68a-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="3f68a-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="3f68a-139">-HostNames</span></span>
<span data-ttu-id="3f68a-140">Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="3f68a-140">Host names</span></span>

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

### <span data-ttu-id="3f68a-141">-Name</span><span class="sxs-lookup"><span data-stu-id="3f68a-141">-Name</span></span>
<span data-ttu-id="3f68a-142">A parancs által összeadott előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f68a-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="3f68a-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3f68a-143">-Protocol</span></span>
<span data-ttu-id="3f68a-144">A HTTP-hallgató protokollját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3f68a-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="3f68a-145">A HTTP és a HTTPS protokoll egyaránt támogatott.</span><span class="sxs-lookup"><span data-stu-id="3f68a-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="3f68a-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="3f68a-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="3f68a-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f68a-147">-SslCertificate</span></span>
<span data-ttu-id="3f68a-148">A HTTP-hallgató SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f68a-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="3f68a-149">Meg kell adni, ha a HTTPS meg van adva hallgató protokollként.</span><span class="sxs-lookup"><span data-stu-id="3f68a-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="3f68a-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="3f68a-150">-SslCertificateId</span></span>
<span data-ttu-id="3f68a-151">A HTTP-hallgató SSL-tanúsítványazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f68a-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="3f68a-152">Meg kell adni, ha a HTTPS protokoll van megadva.</span><span class="sxs-lookup"><span data-stu-id="3f68a-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="3f68a-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="3f68a-153">-SslProfile</span></span>
<span data-ttu-id="3f68a-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="3f68a-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f68a-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="3f68a-155">-SslProfileId</span></span>
<span data-ttu-id="3f68a-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="3f68a-156">SslProfileId</span></span>

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

### <span data-ttu-id="3f68a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f68a-157">CommonParameters</span></span>
<span data-ttu-id="3f68a-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f68a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f68a-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f68a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f68a-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f68a-160">INPUTS</span></span>

### <span data-ttu-id="3f68a-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f68a-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f68a-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f68a-162">OUTPUTS</span></span>

### <span data-ttu-id="3f68a-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f68a-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f68a-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f68a-164">NOTES</span></span>

## <span data-ttu-id="3f68a-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f68a-165">RELATED LINKS</span></span>

[<span data-ttu-id="3f68a-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f68a-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3f68a-167">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f68a-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3f68a-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f68a-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3f68a-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f68a-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


