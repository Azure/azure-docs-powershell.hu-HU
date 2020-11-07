---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: bda8ce00d316d57522bb307518c535c591e7b602
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850813"
---
# <span data-ttu-id="4c304-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c304-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4c304-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c304-102">SYNOPSIS</span></span>
<span data-ttu-id="4c304-103">HTTP-figyelőt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4c304-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c304-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c304-104">SYNTAX</span></span>

### <span data-ttu-id="4c304-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c304-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c304-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4c304-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c304-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c304-107">DESCRIPTION</span></span>
<span data-ttu-id="4c304-108">Az **Add-AzureRmApplicationGatewayHttpListener** PARANCSMAG egy http-figyelőt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4c304-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="4c304-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4c304-109">EXAMPLES</span></span>

### <span data-ttu-id="4c304-110">1. példa: HTTP-figyelő felvétele</span><span class="sxs-lookup"><span data-stu-id="4c304-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="4c304-111">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja. A második parancs hozzáadja a HTTP-figyelőt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4c304-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="4c304-112">2. példa: HTTPS-figyelő felvétele SSL-lel</span><span class="sxs-lookup"><span data-stu-id="4c304-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="4c304-113">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c304-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4c304-114">A második parancs hozzáadja azt a figyelőt, amely a HTTPS protokollt használja az Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="4c304-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="4c304-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c304-115">PARAMETERS</span></span>

### <span data-ttu-id="4c304-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c304-116">-ApplicationGateway</span></span>
<span data-ttu-id="4c304-117">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag hozzáadja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="4c304-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="4c304-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c304-118">-DefaultProfile</span></span>
<span data-ttu-id="4c304-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c304-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c304-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c304-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="4c304-121">Az Application Gateway előtér IP-erőforrás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-121">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c304-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4c304-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="4c304-123">Az Application Gateway előtér IP-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="4c304-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c304-124">-FrontendPort</span></span>
<span data-ttu-id="4c304-125">Az alkalmazás-átjáró előtér-port objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-125">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c304-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="4c304-126">-FrontendPortId</span></span>
<span data-ttu-id="4c304-127">Az Application Gateway előtér-port AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="4c304-128">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="4c304-128">-HostName</span></span>
<span data-ttu-id="4c304-129">Annak az állomásnak a neve, amelyhez a parancsmag hozzáadja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="4c304-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c304-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c304-130">-Name</span></span>
<span data-ttu-id="4c304-131">A parancs által hozzáadott előtér-végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="4c304-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4c304-132">-Protocol</span></span>
<span data-ttu-id="4c304-133">A HTTP-figyelő protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="4c304-134">A HTTP és a HTTPS egyaránt támogatott.</span><span class="sxs-lookup"><span data-stu-id="4c304-134">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c304-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="4c304-135">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c304-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="4c304-136">-SslCertificate</span></span>
<span data-ttu-id="4c304-137">A HTTP-figyelő SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="4c304-138">Meg kell adni, ha a HTTPS a figyelő protokollként van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="4c304-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c304-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="4c304-139">-SslCertificateId</span></span>
<span data-ttu-id="4c304-140">A HTTP-figyelő SSL-tanúsítványának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c304-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="4c304-141">Meg kell adni, ha a HTTPS a figyelő protokollként van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="4c304-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="4c304-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c304-142">CommonParameters</span></span>
<span data-ttu-id="4c304-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c304-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c304-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c304-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c304-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c304-145">INPUTS</span></span>

### <span data-ttu-id="4c304-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4c304-146">System.String</span></span>

## <span data-ttu-id="4c304-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c304-147">OUTPUTS</span></span>

### <span data-ttu-id="4c304-148">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c304-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c304-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c304-149">NOTES</span></span>

## <span data-ttu-id="4c304-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c304-150">RELATED LINKS</span></span>

[<span data-ttu-id="4c304-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c304-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4c304-152">Új – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c304-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4c304-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c304-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4c304-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c304-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


