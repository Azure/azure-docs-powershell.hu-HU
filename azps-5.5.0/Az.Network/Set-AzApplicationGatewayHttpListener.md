---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156786"
---
# <span data-ttu-id="5ee92-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ee92-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5ee92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ee92-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee92-103">Módosít egy HTTP-hallgatót egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5ee92-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="5ee92-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ee92-104">SYNTAX</span></span>

### <span data-ttu-id="5ee92-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ee92-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ee92-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5ee92-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ee92-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ee92-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee92-108">A **Set-AzApplicationGatewayHttpListener** parancsmag módosítja az Azure-alkalmazásátjárók HTTP-figyelőit.</span><span class="sxs-lookup"><span data-stu-id="5ee92-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="5ee92-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ee92-109">EXAMPLES</span></span>

### <span data-ttu-id="5ee92-110">1. példa: HTTP-hallgató beállítása</span><span class="sxs-lookup"><span data-stu-id="5ee92-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="5ee92-111">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ee92-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5ee92-112">A második parancs úgy állítja be az átjáró HTTP-hallgatóját, hogy az $FIP 01-ben tárolt előlapi konfigurációt használja a 80-as portON található HTTP-protokollal.</span><span class="sxs-lookup"><span data-stu-id="5ee92-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="5ee92-113">2. példa: HTTPS-hallgató hozzáadása SSL és HostNames szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="5ee92-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="5ee92-114">Az első parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ee92-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5ee92-115">A második parancs hozzáadja a hallgatót, amely a HTTPS protokollt használja SSL-tanúsítványokkal és HostNames-ekkel együtt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5ee92-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="5ee92-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ee92-116">PARAMETERS</span></span>

### <span data-ttu-id="5ee92-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ee92-117">-ApplicationGateway</span></span>
<span data-ttu-id="5ee92-118">Azt az alkalmazás-átjárót adja meg, amellyel a parancsmag társítja a HTTP-et.</span><span class="sxs-lookup"><span data-stu-id="5ee92-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="5ee92-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ee92-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="5ee92-120">Ügyfélhiba egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="5ee92-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="5ee92-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee92-121">-DefaultProfile</span></span>
<span data-ttu-id="5ee92-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ee92-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee92-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5ee92-123">-FirewallPolicy</span></span>
<span data-ttu-id="5ee92-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5ee92-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="5ee92-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5ee92-125">-FirewallPolicyId</span></span>
<span data-ttu-id="5ee92-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5ee92-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="5ee92-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ee92-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="5ee92-128">Az alkalmazás átjárója előlapi IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee92-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="5ee92-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5ee92-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="5ee92-130">Az alkalmazás-átjáró előlapi IP-címének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5ee92-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="5ee92-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="5ee92-131">-FrontendPort</span></span>
<span data-ttu-id="5ee92-132">Az alkalmazás átjárójának előlapi portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee92-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="5ee92-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="5ee92-133">-FrontendPortId</span></span>
<span data-ttu-id="5ee92-134">Az alkalmazás átjárójának előlapi portazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee92-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="5ee92-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="5ee92-135">-HostName</span></span>
<span data-ttu-id="5ee92-136">Megadja azt az állomásnevet, amelybe a parancsmag elküldi a HTTP-et.</span><span class="sxs-lookup"><span data-stu-id="5ee92-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="5ee92-137">-HostNames</span><span class="sxs-lookup"><span data-stu-id="5ee92-137">-HostNames</span></span>
<span data-ttu-id="5ee92-138">Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="5ee92-138">Host names</span></span>

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

### <span data-ttu-id="5ee92-139">-Name</span><span class="sxs-lookup"><span data-stu-id="5ee92-139">-Name</span></span>
<span data-ttu-id="5ee92-140">A HTTP-hallgató nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee92-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="5ee92-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5ee92-141">-Protocol</span></span>
<span data-ttu-id="5ee92-142">A HTTP-halló által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee92-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="5ee92-143">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5ee92-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5ee92-144">Http</span><span class="sxs-lookup"><span data-stu-id="5ee92-144">Http</span></span>
- <span data-ttu-id="5ee92-145">Https</span><span class="sxs-lookup"><span data-stu-id="5ee92-145">Https</span></span>

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

### <span data-ttu-id="5ee92-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="5ee92-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="5ee92-147">Azt adja meg, hogy a parancsmagnak meg kell-e adhatja a kiszolgáló nevének jelzését.</span><span class="sxs-lookup"><span data-stu-id="5ee92-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="5ee92-148">A paraméter elfogadható értékei: igaz vagy hamis.</span><span class="sxs-lookup"><span data-stu-id="5ee92-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="5ee92-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ee92-149">-SslCertificate</span></span>
<span data-ttu-id="5ee92-150">A HTTP-hallgató SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee92-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="5ee92-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="5ee92-151">-SslCertificateId</span></span>
<span data-ttu-id="5ee92-152">A HTTP-halló SSL-tanúsítványazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ee92-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="5ee92-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="5ee92-153">-SslProfile</span></span>
<span data-ttu-id="5ee92-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="5ee92-154">SslProfile</span></span>

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

### <span data-ttu-id="5ee92-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="5ee92-155">-SslProfileId</span></span>
<span data-ttu-id="5ee92-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="5ee92-156">SslProfileId</span></span>

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

### <span data-ttu-id="5ee92-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee92-157">CommonParameters</span></span>
<span data-ttu-id="5ee92-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee92-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee92-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ee92-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee92-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ee92-160">INPUTS</span></span>

### <span data-ttu-id="5ee92-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ee92-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ee92-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ee92-162">OUTPUTS</span></span>

### <span data-ttu-id="5ee92-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ee92-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ee92-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ee92-164">NOTES</span></span>

## <span data-ttu-id="5ee92-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ee92-165">RELATED LINKS</span></span>

[<span data-ttu-id="5ee92-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ee92-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ee92-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ee92-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ee92-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ee92-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ee92-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ee92-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


