---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014799"
---
# <span data-ttu-id="53abf-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53abf-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="53abf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53abf-102">SYNOPSIS</span></span>
<span data-ttu-id="53abf-103">HTTP-figyelőt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="53abf-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="53abf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53abf-104">SYNTAX</span></span>

### <span data-ttu-id="53abf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53abf-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53abf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="53abf-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53abf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="53abf-107">DESCRIPTION</span></span>
<span data-ttu-id="53abf-108">A **New-AzApplicationGatewayHttpListener** parancsmag létrehoz egy http-figyelőt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="53abf-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="53abf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="53abf-109">EXAMPLES</span></span>

### <span data-ttu-id="53abf-110">Példa 1: HTTP-figyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="53abf-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="53abf-111">Ez a parancs létrehoz egy Listener01 nevű HTTP-figyelőt, és az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="53abf-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="53abf-112">2. példa: HTTP-figyelő létrehozása SSL-lel</span><span class="sxs-lookup"><span data-stu-id="53abf-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="53abf-113">Ez a parancs létrehoz egy SSL-tehermentesítést használó HTTP-figyelőt, és megadja az SSL-tanúsítványt a $SSLCert 01 változóban.</span><span class="sxs-lookup"><span data-stu-id="53abf-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="53abf-114">A parancs az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="53abf-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="53abf-115">3. példa: HTTP-figyelő létrehozása tűzfal-házirenddel</span><span class="sxs-lookup"><span data-stu-id="53abf-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="53abf-116">Ez a parancs létrehoz egy Listener01 nevű HTTP-figyelőt, a FirewallPolicy $firewallPolicy, és az eredményt a $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="53abf-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="53abf-117">Példa 4: HTTPS-figyelő hozzáadása SSL-és állomásnevek használatával</span><span class="sxs-lookup"><span data-stu-id="53abf-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="53abf-118">Ez a parancs létrehoz egy SSL-tehermentesítést használó HTTP-figyelőt, és az SSL-tanúsítványt a $SSLCert 01 változóban két állomásnévvel együtt adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="53abf-119">A parancs az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="53abf-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="53abf-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53abf-120">PARAMETERS</span></span>

### <span data-ttu-id="53abf-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="53abf-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="53abf-122">Az alkalmazás-átjáró ügyfél-hibája</span><span class="sxs-lookup"><span data-stu-id="53abf-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="53abf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53abf-123">-DefaultProfile</span></span>
<span data-ttu-id="53abf-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53abf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53abf-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="53abf-125">-FirewallPolicy</span></span>
<span data-ttu-id="53abf-126">A legfelső szintű tűzfal-házirendre mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="53abf-127">Az objektum hivatkozását New-AzApplicationGatewayWebApplicationFirewallPolicy parancsmag használatával lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="53abf-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="53abf-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" a fenti parancsmagot létrehozott tűzfal-házirendet az elérési út szabályi szintjén lehet megtekinteni.</span><span class="sxs-lookup"><span data-stu-id="53abf-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="53abf-129">a parancs a fenti paranccsal létrehozta az alapértelmezett házirend-beállításokat és felügyelt szabályokat.</span><span class="sxs-lookup"><span data-stu-id="53abf-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="53abf-130">Az alapértelmezett értékek helyett a felhasználók megadhatják a PolicySettings, az ManagedRules és New-AzApplicationGatewayFirewallPolicySettings a New-AzApplicationGatewayFirewallPolicyManagedRulest is.</span><span class="sxs-lookup"><span data-stu-id="53abf-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="53abf-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="53abf-131">-FirewallPolicyId</span></span>
<span data-ttu-id="53abf-132">Egy meglévő, legfelső szintű webalkalmazás-tűzfal-erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="53abf-133">A tűzfal-házirend azonosítóit a Get-AzApplicationGatewayWebApplicationFirewallPolicy parancsmag segítségével lehet visszaadni.</span><span class="sxs-lookup"><span data-stu-id="53abf-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="53abf-134">Miután rendelkezünk az AZONOSÍTÓval, a *FirewallPolicy* paraméter helyett használhatja a *FirewallPolicyId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="53abf-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="53abf-135">Például:-FirewallPolicyId/Subscriptions/<előfizetés-azonosító>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="53abf-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="53abf-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53abf-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="53abf-137">A HTTP-figyelő előtér IP-konfigurációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="53abf-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="53abf-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="53abf-139">A HTTP-figyelő előtér-IP-konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="53abf-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="53abf-140">-FrontendPort</span></span>
<span data-ttu-id="53abf-141">A HTTP-figyelő előtér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="53abf-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="53abf-142">-FrontendPortId</span></span>
<span data-ttu-id="53abf-143">A HTTP-figyelőhöz tartozó előtér-objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="53abf-144">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="53abf-144">-HostName</span></span>
<span data-ttu-id="53abf-145">Az alkalmazás-átjáró HTTP-figyelő állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="53abf-146">-Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="53abf-146">-HostNames</span></span>
<span data-ttu-id="53abf-147">Állomásnevek</span><span class="sxs-lookup"><span data-stu-id="53abf-147">Host names</span></span>

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

### <span data-ttu-id="53abf-148">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53abf-148">-Name</span></span>
<span data-ttu-id="53abf-149">Megadja annak a HTTP-figyelőnek a nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="53abf-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="53abf-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="53abf-150">-Protocol</span></span>
<span data-ttu-id="53abf-151">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="53abf-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="53abf-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="53abf-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="53abf-153">-SslCertificate</span></span>
<span data-ttu-id="53abf-154">A HTTP-figyelő SSL-tanúsítvány objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="53abf-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="53abf-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="53abf-155">-SslCertificateId</span></span>
<span data-ttu-id="53abf-156">Az SSL-tanúsítvány AZONOSÍTÓját adja meg a HTTP-figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="53abf-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="53abf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53abf-157">CommonParameters</span></span>
<span data-ttu-id="53abf-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53abf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53abf-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53abf-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53abf-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53abf-160">INPUTS</span></span>

### <span data-ttu-id="53abf-161">Nincs</span><span class="sxs-lookup"><span data-stu-id="53abf-161">None</span></span>

## <span data-ttu-id="53abf-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53abf-162">OUTPUTS</span></span>

### <span data-ttu-id="53abf-163">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53abf-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="53abf-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53abf-164">NOTES</span></span>

## <span data-ttu-id="53abf-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53abf-165">RELATED LINKS</span></span>

[<span data-ttu-id="53abf-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53abf-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="53abf-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53abf-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="53abf-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53abf-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="53abf-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="53abf-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


