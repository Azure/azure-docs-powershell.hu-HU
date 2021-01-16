---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: a6fc3eb16cc82f7a0964e8cd0c1697a083771016
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351881"
---
# <span data-ttu-id="64bef-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64bef-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="64bef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bef-102">SYNOPSIS</span></span>
<span data-ttu-id="64bef-103">HTTP-hallgatót hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="64bef-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="64bef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64bef-104">SYNTAX</span></span>

### <span data-ttu-id="64bef-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64bef-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64bef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="64bef-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64bef-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64bef-107">DESCRIPTION</span></span>
<span data-ttu-id="64bef-108">A **New-AzApplicationGatewayHttpListener** parancsmag létrehoz egy HTTP-hallgatót egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="64bef-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="64bef-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64bef-109">EXAMPLES</span></span>

### <span data-ttu-id="64bef-110">1. példa: HTTP-hallgató létrehozása</span><span class="sxs-lookup"><span data-stu-id="64bef-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="64bef-111">Ez a parancs létrehoz egy Listener01 nevű HTTP-hallgatót, és az eredményt a "$Listener" változóban $Listener.</span><span class="sxs-lookup"><span data-stu-id="64bef-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="64bef-112">2. példa: HTTP-hallgató létrehozása SSL-sel</span><span class="sxs-lookup"><span data-stu-id="64bef-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="64bef-113">Ez a parancs létrehoz egy OLYAN HTTP-hallgatót, amely az SSL-t betölti, és biztosítja az SSL-tanúsítványt a $SSLCert 01 változóban.</span><span class="sxs-lookup"><span data-stu-id="64bef-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="64bef-114">A parancs az eredményt a következő nevű változóban $Listener.</span><span class="sxs-lookup"><span data-stu-id="64bef-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="64bef-115">3. példa: HTTP-hallgató létrehozása tűzfal-házirend használatával</span><span class="sxs-lookup"><span data-stu-id="64bef-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="64bef-116">Ez a parancs létrehoz egy Listener01 (FirewallPolicy mint $firewallPolicy) nevű HTTP-hallgatót, és az eredményt egy "$Listener" nevű változóban $Listener.</span><span class="sxs-lookup"><span data-stu-id="64bef-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="64bef-117">4. példa: HTTPS-hallgató hozzáadása SSL és HostNames szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="64bef-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="64bef-118">Ez a parancs létrehoz egy OLYAN HTTP-hallgatót, amely az SSL-t betölti, és a $SSLCert 01 változóban biztosítja az SSL-tanúsítványt két HostNames szolgáltatóval együtt.</span><span class="sxs-lookup"><span data-stu-id="64bef-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="64bef-119">A parancs az eredményt a következő nevű változóban $Listener.</span><span class="sxs-lookup"><span data-stu-id="64bef-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="64bef-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64bef-120">PARAMETERS</span></span>

### <span data-ttu-id="64bef-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="64bef-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="64bef-122">Ügyfélhiba egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="64bef-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="64bef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bef-123">-DefaultProfile</span></span>
<span data-ttu-id="64bef-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64bef-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64bef-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="64bef-125">-FirewallPolicy</span></span>
<span data-ttu-id="64bef-126">Egy legfelső szintű tűzfal-házirend objektumhivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="64bef-127">Az objektumhivatkozást egy parancsmag használatával New-AzApplicationGatewayWebApplicationFirewallPolicy létrehozni.</span><span class="sxs-lookup"><span data-stu-id="64bef-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="64bef-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A fenti parancsmag használatával létrehozott tűzfalházi házirendre elérésiút-szabályszinten hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="64bef-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="64bef-129">he above command would create a default policy settings and managed rules.</span><span class="sxs-lookup"><span data-stu-id="64bef-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="64bef-130">Az alapértelmezett értékek helyett a felhasználók megadhatják a PolicySettings és a ManagedRules beállítást a New-AzApplicationGatewayFirewallPolicySettings és New-AzApplicationGatewayFirewallPolicyManagedRules meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="64bef-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="64bef-131">-FirewallPolicyId</span></span>
<span data-ttu-id="64bef-132">Egy meglévő legfelső szintű webalkalmazás tűzfalerőforrásának azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="64bef-133">A tűzfalháziaktár-okat a parancsmag Get-AzApplicationGatewayWebApplicationFirewallPolicy vissza.</span><span class="sxs-lookup"><span data-stu-id="64bef-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="64bef-134">Az azonosító megadása után a *FirewallPolicyId* paramétert használhatja a *FirewallPolicy paraméter helyett.*</span><span class="sxs-lookup"><span data-stu-id="64bef-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="64bef-135">Például: -FirewallPolicyId /subscriptions/<előfizetés-azonosító>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="64bef-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="64bef-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64bef-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="64bef-137">A HTTP-halló előlapi IP-konfigurációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="64bef-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="64bef-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="64bef-139">A HTTP-halló előlapi IP-konfigurációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64bef-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="64bef-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="64bef-140">-FrontendPort</span></span>
<span data-ttu-id="64bef-141">A HTTP-hallgató előlapi portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="64bef-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="64bef-142">-FrontendPortId</span></span>
<span data-ttu-id="64bef-143">A HTTP-halló előlapi portobjektumának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64bef-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="64bef-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="64bef-144">-HostName</span></span>
<span data-ttu-id="64bef-145">Az alkalmazás-átjáró HTTP- hallgató állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="64bef-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="64bef-146">-HostNames</span></span>
<span data-ttu-id="64bef-147">Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="64bef-147">Host names</span></span>

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

### <span data-ttu-id="64bef-148">-Name</span><span class="sxs-lookup"><span data-stu-id="64bef-148">-Name</span></span>
<span data-ttu-id="64bef-149">A parancsmag által létrehozott HTTP-hallgató nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="64bef-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="64bef-150">-Protocol</span></span>
<span data-ttu-id="64bef-151">A HTTP-halló által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="64bef-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="64bef-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64bef-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="64bef-153">-SslCertificate</span></span>
<span data-ttu-id="64bef-154">A HTTP-hallgató SSL-tanúsítványobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64bef-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="64bef-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="64bef-155">-SslCertificateId</span></span>
<span data-ttu-id="64bef-156">A HTTP-hallgató SSL-tanúsítványának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64bef-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="64bef-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="64bef-157">-SslProfile</span></span>
<span data-ttu-id="64bef-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="64bef-158">SslProfile</span></span>

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

### <span data-ttu-id="64bef-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="64bef-159">-SslProfileId</span></span>
<span data-ttu-id="64bef-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="64bef-160">SslProfileId</span></span>

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

### <span data-ttu-id="64bef-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bef-161">CommonParameters</span></span>
<span data-ttu-id="64bef-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bef-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bef-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64bef-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bef-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64bef-164">INPUTS</span></span>

### <span data-ttu-id="64bef-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="64bef-165">None</span></span>

## <span data-ttu-id="64bef-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64bef-166">OUTPUTS</span></span>

### <span data-ttu-id="64bef-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64bef-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="64bef-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64bef-168">NOTES</span></span>

## <span data-ttu-id="64bef-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64bef-169">RELATED LINKS</span></span>

[<span data-ttu-id="64bef-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64bef-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="64bef-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64bef-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="64bef-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64bef-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="64bef-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="64bef-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


