---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837804"
---
# <span data-ttu-id="3ea31-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ea31-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3ea31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ea31-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea31-103">Az alkalmazás-átjárók HTTP-figyelését módosítja.</span><span class="sxs-lookup"><span data-stu-id="3ea31-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="3ea31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ea31-104">SYNTAX</span></span>

### <span data-ttu-id="3ea31-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ea31-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ea31-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3ea31-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ea31-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ea31-107">DESCRIPTION</span></span>
<span data-ttu-id="3ea31-108">A **set-AzApplicationGatewayHttpListener** parancsmag módosította az Azure Application ÁTJÁRÓk http-figyelőjét.</span><span class="sxs-lookup"><span data-stu-id="3ea31-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="3ea31-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3ea31-109">EXAMPLES</span></span>

### <span data-ttu-id="3ea31-110">Példa 1: HTTP-figyelő beállítása</span><span class="sxs-lookup"><span data-stu-id="3ea31-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="3ea31-111">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3ea31-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3ea31-112">A második parancs az átjáróhoz tartozó HTTP-figyelőt állítja be a 80 $FIP-on tárolt, az előtér-konfigurációban lévő HTTP-protokollon keresztül.</span><span class="sxs-lookup"><span data-stu-id="3ea31-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="3ea31-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ea31-113">PARAMETERS</span></span>

### <span data-ttu-id="3ea31-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ea31-114">-ApplicationGateway</span></span>
<span data-ttu-id="3ea31-115">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag társítja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="3ea31-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="3ea31-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ea31-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="3ea31-117">Az alkalmazás-átjáró ügyfél-hibája</span><span class="sxs-lookup"><span data-stu-id="3ea31-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="3ea31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea31-118">-DefaultProfile</span></span>
<span data-ttu-id="3ea31-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ea31-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ea31-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ea31-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="3ea31-121">Az alkalmazás-átjáró előtér IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea31-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3ea31-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3ea31-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="3ea31-123">Az alkalmazás-átjáró előtér-IP-címének AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea31-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3ea31-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3ea31-124">-FrontendPort</span></span>
<span data-ttu-id="3ea31-125">Az Application Gateway előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea31-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="3ea31-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="3ea31-126">-FrontendPortId</span></span>
<span data-ttu-id="3ea31-127">Az Application Gateway előtér-port AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea31-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="3ea31-128">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="3ea31-128">-HostName</span></span>
<span data-ttu-id="3ea31-129">Azt az állomásnevet adja meg, amelyre a parancsmag a HTTP-figyelőt elküldi.</span><span class="sxs-lookup"><span data-stu-id="3ea31-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="3ea31-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ea31-130">-Name</span></span>
<span data-ttu-id="3ea31-131">A HTTP-figyelő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea31-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="3ea31-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3ea31-132">-Protocol</span></span>
<span data-ttu-id="3ea31-133">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea31-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="3ea31-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3ea31-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ea31-135">Http</span><span class="sxs-lookup"><span data-stu-id="3ea31-135">Http</span></span>
- <span data-ttu-id="3ea31-136">Https</span><span class="sxs-lookup"><span data-stu-id="3ea31-136">Https</span></span>

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

### <span data-ttu-id="3ea31-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="3ea31-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="3ea31-138">Azt adja meg, hogy a parancsmagnak meg kell-e adni a kiszolgálónév jelzését.</span><span class="sxs-lookup"><span data-stu-id="3ea31-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="3ea31-139">A paraméter elfogadható értékei a következők: igaz vagy hamis.</span><span class="sxs-lookup"><span data-stu-id="3ea31-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="3ea31-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ea31-140">-SslCertificate</span></span>
<span data-ttu-id="3ea31-141">A HTTP-figyelő SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea31-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="3ea31-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="3ea31-142">-SslCertificateId</span></span>
<span data-ttu-id="3ea31-143">Megadja a HTTP-figyelő Secure Socket Layer (SSL) tanúsítvány-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="3ea31-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="3ea31-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea31-144">CommonParameters</span></span>
<span data-ttu-id="3ea31-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ea31-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea31-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea31-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea31-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ea31-147">INPUTS</span></span>

### <span data-ttu-id="3ea31-148">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ea31-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ea31-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ea31-149">OUTPUTS</span></span>

### <span data-ttu-id="3ea31-150">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ea31-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ea31-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ea31-151">NOTES</span></span>

## <span data-ttu-id="3ea31-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ea31-152">RELATED LINKS</span></span>

[<span data-ttu-id="3ea31-153">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ea31-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3ea31-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ea31-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3ea31-155">Új – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ea31-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3ea31-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ea31-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


