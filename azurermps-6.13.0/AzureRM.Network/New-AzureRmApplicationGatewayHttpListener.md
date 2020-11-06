---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 29df7c4ac7cb941e8826c3e1fb929d92cc626512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500215"
---
# <span data-ttu-id="fe3e7-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe3e7-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fe3e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe3e7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3e7-103">HTTP-figyelőt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe3e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe3e7-104">SYNTAX</span></span>

### <span data-ttu-id="fe3e7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3e7-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe3e7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fe3e7-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3e7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe3e7-107">DESCRIPTION</span></span>
<span data-ttu-id="fe3e7-108">A **New-AzureRmApplicationGatewayHttpListener** parancsmag létrehoz egy http-figyelőt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="fe3e7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fe3e7-109">EXAMPLES</span></span>

### <span data-ttu-id="fe3e7-110">Példa 1: HTTP-figyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe3e7-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="fe3e7-111">Ez a parancs létrehoz egy Listener01 nevű HTTP-figyelőt, és az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="fe3e7-112">2. példa: HTTP-figyelő létrehozása SSL-lel</span><span class="sxs-lookup"><span data-stu-id="fe3e7-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="fe3e7-113">Ez a parancs létrehoz egy SSL-tehermentesítést használó HTTP-figyelőt, és megadja az SSL-tanúsítványt a $SSLCert 01 változóban.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="fe3e7-114">A parancs az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="fe3e7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe3e7-115">PARAMETERS</span></span>

### <span data-ttu-id="fe3e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3e7-116">-DefaultProfile</span></span>
<span data-ttu-id="fe3e7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe3e7-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe3e7-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="fe3e7-119">A HTTP-figyelő előtér IP-konfigurációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="fe3e7-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fe3e7-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="fe3e7-121">A HTTP-figyelő előtér-IP-konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="fe3e7-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="fe3e7-122">-FrontendPort</span></span>
<span data-ttu-id="fe3e7-123">A HTTP-figyelő előtér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="fe3e7-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="fe3e7-124">-FrontendPortId</span></span>
<span data-ttu-id="fe3e7-125">A HTTP-figyelőhöz tartozó előtér-objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="fe3e7-126">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="fe3e7-126">-HostName</span></span>
<span data-ttu-id="fe3e7-127">Az alkalmazás-átjáró HTTP-figyelő állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="fe3e7-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe3e7-128">-Name</span></span>
<span data-ttu-id="fe3e7-129">Megadja annak a HTTP-figyelőnek a nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe3e7-130">-Protocol</span><span class="sxs-lookup"><span data-stu-id="fe3e7-130">-Protocol</span></span>
<span data-ttu-id="fe3e7-131">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="fe3e7-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="fe3e7-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="fe3e7-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe3e7-133">-SslCertificate</span></span>
<span data-ttu-id="fe3e7-134">A HTTP-figyelő SSL-tanúsítvány objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="fe3e7-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="fe3e7-135">-SslCertificateId</span></span>
<span data-ttu-id="fe3e7-136">Az SSL-tanúsítvány AZONOSÍTÓját adja meg a HTTP-figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="fe3e7-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="fe3e7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3e7-137">CommonParameters</span></span>
<span data-ttu-id="fe3e7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe3e7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3e7-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe3e7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3e7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe3e7-140">INPUTS</span></span>

### <span data-ttu-id="fe3e7-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe3e7-141">None</span></span>

## <span data-ttu-id="fe3e7-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe3e7-142">OUTPUTS</span></span>

### <span data-ttu-id="fe3e7-143">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe3e7-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fe3e7-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe3e7-144">NOTES</span></span>

## <span data-ttu-id="fe3e7-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe3e7-145">RELATED LINKS</span></span>

[<span data-ttu-id="fe3e7-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe3e7-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe3e7-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe3e7-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe3e7-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe3e7-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe3e7-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe3e7-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


