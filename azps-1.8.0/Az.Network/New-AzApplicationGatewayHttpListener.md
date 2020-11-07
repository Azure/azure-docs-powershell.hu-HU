---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670407"
---
# <span data-ttu-id="5c1a7-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5c1a7-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5c1a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c1a7-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1a7-103">HTTP-figyelőt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="5c1a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c1a7-104">SYNTAX</span></span>

### <span data-ttu-id="5c1a7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c1a7-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c1a7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5c1a7-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c1a7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c1a7-107">DESCRIPTION</span></span>
<span data-ttu-id="5c1a7-108">A **New-AzApplicationGatewayHttpListener** parancsmag létrehoz egy http-figyelőt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="5c1a7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5c1a7-109">EXAMPLES</span></span>

### <span data-ttu-id="5c1a7-110">Példa 1: HTTP-figyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="5c1a7-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="5c1a7-111">Ez a parancs létrehoz egy Listener01 nevű HTTP-figyelőt, és az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="5c1a7-112">2. példa: HTTP-figyelő létrehozása SSL-lel</span><span class="sxs-lookup"><span data-stu-id="5c1a7-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="5c1a7-113">Ez a parancs létrehoz egy SSL-tehermentesítést használó HTTP-figyelőt, és megadja az SSL-tanúsítványt a $SSLCert 01 változóban.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="5c1a7-114">A parancs az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="5c1a7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c1a7-115">PARAMETERS</span></span>

### <span data-ttu-id="5c1a7-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c1a7-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="5c1a7-117">Az alkalmazás-átjáró ügyfél-hibája</span><span class="sxs-lookup"><span data-stu-id="5c1a7-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="5c1a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1a7-118">-DefaultProfile</span></span>
<span data-ttu-id="5c1a7-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c1a7-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c1a7-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="5c1a7-121">A HTTP-figyelő előtér IP-konfigurációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="5c1a7-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5c1a7-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="5c1a7-123">A HTTP-figyelő előtér-IP-konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="5c1a7-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="5c1a7-124">-FrontendPort</span></span>
<span data-ttu-id="5c1a7-125">A HTTP-figyelő előtér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="5c1a7-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="5c1a7-126">-FrontendPortId</span></span>
<span data-ttu-id="5c1a7-127">A HTTP-figyelőhöz tartozó előtér-objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="5c1a7-128">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="5c1a7-128">-HostName</span></span>
<span data-ttu-id="5c1a7-129">Az alkalmazás-átjáró HTTP-figyelő állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="5c1a7-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5c1a7-130">-Name</span></span>
<span data-ttu-id="5c1a7-131">Megadja annak a HTTP-figyelőnek a nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5c1a7-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5c1a7-132">-Protocol</span></span>
<span data-ttu-id="5c1a7-133">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="5c1a7-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="5c1a7-134">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="5c1a7-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c1a7-135">-SslCertificate</span></span>
<span data-ttu-id="5c1a7-136">A HTTP-figyelő SSL-tanúsítvány objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="5c1a7-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="5c1a7-137">-SslCertificateId</span></span>
<span data-ttu-id="5c1a7-138">Az SSL-tanúsítvány AZONOSÍTÓját adja meg a HTTP-figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="5c1a7-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="5c1a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1a7-139">CommonParameters</span></span>
<span data-ttu-id="5c1a7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c1a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1a7-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1a7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1a7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c1a7-142">INPUTS</span></span>

### <span data-ttu-id="5c1a7-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="5c1a7-143">None</span></span>

## <span data-ttu-id="5c1a7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c1a7-144">OUTPUTS</span></span>

### <span data-ttu-id="5c1a7-145">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5c1a7-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5c1a7-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c1a7-146">NOTES</span></span>

## <span data-ttu-id="5c1a7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c1a7-147">RELATED LINKS</span></span>

[<span data-ttu-id="5c1a7-148">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5c1a7-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5c1a7-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5c1a7-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5c1a7-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5c1a7-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5c1a7-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5c1a7-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


