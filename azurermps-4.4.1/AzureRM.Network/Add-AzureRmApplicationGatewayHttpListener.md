---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6cf8dc5ab895ac59697b10494f7f39d158238d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680259"
---
# <span data-ttu-id="d1e6a-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1e6a-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d1e6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e6a-103">HTTP-figyelőt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1e6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1e6a-104">SYNTAX</span></span>

### <span data-ttu-id="d1e6a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1e6a-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1e6a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d1e6a-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1e6a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1e6a-107">DESCRIPTION</span></span>
<span data-ttu-id="d1e6a-108">Az **Add-AzureRmApplicationGatewayHttpListener** PARANCSMAG egy http-figyelőt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="d1e6a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d1e6a-109">EXAMPLES</span></span>

### <span data-ttu-id="d1e6a-110">1. példa: HTTP-figyelő felvétele</span><span class="sxs-lookup"><span data-stu-id="d1e6a-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="d1e6a-111">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs hozzáadja a HTTP-figyelőt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="d1e6a-112">2. példa: HTTPS-figyelő felvétele SSL-lel</span><span class="sxs-lookup"><span data-stu-id="d1e6a-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="d1e6a-113">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d1e6a-114">A második parancs hozzáadja azt a figyelőt, amely a HTTPS protokollt használja az Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="d1e6a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1e6a-115">PARAMETERS</span></span>

### <span data-ttu-id="d1e6a-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1e6a-116">-ApplicationGateway</span></span>
<span data-ttu-id="d1e6a-117">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag hozzáadja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="d1e6a-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1e6a-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d1e6a-119">Az Application Gateway előtér IP-erőforrás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-119">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="d1e6a-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d1e6a-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d1e6a-121">Az Application Gateway előtér IP-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-121">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="d1e6a-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1e6a-122">-FrontendPort</span></span>
<span data-ttu-id="d1e6a-123">Az alkalmazás-átjáró előtér-port objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-123">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="d1e6a-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="d1e6a-124">-FrontendPortId</span></span>
<span data-ttu-id="d1e6a-125">Az Application Gateway előtér-port AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="d1e6a-126">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="d1e6a-126">-HostName</span></span>
<span data-ttu-id="d1e6a-127">Annak az állomásnak a neve, amelyhez a parancsmag hozzáadja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-127">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="d1e6a-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1e6a-128">-Name</span></span>
<span data-ttu-id="d1e6a-129">A parancs által hozzáadott előtér-végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-129">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="d1e6a-130">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d1e6a-130">-Protocol</span></span>
<span data-ttu-id="d1e6a-131">A HTTP-figyelő protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-131">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="d1e6a-132">A HTTP és a HTTPS egyaránt támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-132">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="d1e6a-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d1e6a-133">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="d1e6a-134">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d1e6a-134">-SslCertificate</span></span>
<span data-ttu-id="d1e6a-135">A HTTP-figyelő SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-135">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="d1e6a-136">Meg kell adni, ha a HTTPS a figyelő protokollként van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-136">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="d1e6a-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="d1e6a-137">-SslCertificateId</span></span>
<span data-ttu-id="d1e6a-138">A HTTP-figyelő SSL-tanúsítványának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-138">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="d1e6a-139">Meg kell adni, ha a HTTPS a figyelő protokollként van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-139">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="d1e6a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e6a-140">-DefaultProfile</span></span>
<span data-ttu-id="d1e6a-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1e6a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e6a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e6a-142">CommonParameters</span></span>
<span data-ttu-id="d1e6a-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1e6a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e6a-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1e6a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e6a-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1e6a-145">INPUTS</span></span>

### <span data-ttu-id="d1e6a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d1e6a-146">System.String</span></span>

## <span data-ttu-id="d1e6a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1e6a-147">OUTPUTS</span></span>

### <span data-ttu-id="d1e6a-148">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1e6a-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1e6a-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1e6a-149">NOTES</span></span>

## <span data-ttu-id="d1e6a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1e6a-150">RELATED LINKS</span></span>

[<span data-ttu-id="d1e6a-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1e6a-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d1e6a-152">Új – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1e6a-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d1e6a-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1e6a-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d1e6a-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1e6a-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


