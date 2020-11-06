---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: aea9bb965424de6797373abd1c5426bba808ea5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500511"
---
# <span data-ttu-id="d6353-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6353-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d6353-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6353-102">SYNOPSIS</span></span>
<span data-ttu-id="d6353-103">HTTP-figyelőt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d6353-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6353-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6353-104">SYNTAX</span></span>

### <span data-ttu-id="d6353-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6353-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6353-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d6353-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6353-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6353-107">DESCRIPTION</span></span>
<span data-ttu-id="d6353-108">A **New-AzureRmApplicationGatewayHttpListener** parancsmag létrehoz egy http-figyelőt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="d6353-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="d6353-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6353-109">EXAMPLES</span></span>

### <span data-ttu-id="d6353-110">Példa 1: HTTP-figyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="d6353-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="d6353-111">Ez a parancs létrehoz egy Listener01 nevű HTTP-figyelőt, és az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6353-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="d6353-112">2. példa: HTTP-figyelő létrehozása SSL-lel</span><span class="sxs-lookup"><span data-stu-id="d6353-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="d6353-113">Ez a parancs létrehoz egy SSL-tehermentesítést használó HTTP-figyelőt, és megadja az SSL-tanúsítványt a $SSLCert 01 változóban.</span><span class="sxs-lookup"><span data-stu-id="d6353-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="d6353-114">A parancs az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6353-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="d6353-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6353-115">PARAMETERS</span></span>

### <span data-ttu-id="d6353-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6353-116">-DefaultProfile</span></span>
<span data-ttu-id="d6353-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6353-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6353-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6353-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d6353-119">A HTTP-figyelő előtér IP-konfigurációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6353-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="d6353-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d6353-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d6353-121">A HTTP-figyelő előtér-IP-konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6353-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="d6353-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d6353-122">-FrontendPort</span></span>
<span data-ttu-id="d6353-123">A HTTP-figyelő előtér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6353-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="d6353-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="d6353-124">-FrontendPortId</span></span>
<span data-ttu-id="d6353-125">A HTTP-figyelőhöz tartozó előtér-objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6353-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="d6353-126">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="d6353-126">-HostName</span></span>
<span data-ttu-id="d6353-127">Az alkalmazás-átjáró HTTP-figyelő állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6353-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="d6353-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6353-128">-Name</span></span>
<span data-ttu-id="d6353-129">Megadja annak a HTTP-figyelőnek a nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d6353-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d6353-130">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d6353-130">-Protocol</span></span>
<span data-ttu-id="d6353-131">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6353-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="d6353-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d6353-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="d6353-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d6353-133">-SslCertificate</span></span>
<span data-ttu-id="d6353-134">A HTTP-figyelő SSL-tanúsítvány objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6353-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="d6353-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="d6353-135">-SslCertificateId</span></span>
<span data-ttu-id="d6353-136">Az SSL-tanúsítvány AZONOSÍTÓját adja meg a HTTP-figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="d6353-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="d6353-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6353-137">CommonParameters</span></span>
<span data-ttu-id="d6353-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6353-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6353-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6353-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6353-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6353-140">INPUTS</span></span>

### <span data-ttu-id="d6353-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d6353-141">System.String</span></span>

## <span data-ttu-id="d6353-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6353-142">OUTPUTS</span></span>

### <span data-ttu-id="d6353-143">Microsoft. Azure. commands. Network. models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6353-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="d6353-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6353-144">NOTES</span></span>

## <span data-ttu-id="d6353-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6353-145">RELATED LINKS</span></span>

[<span data-ttu-id="d6353-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6353-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d6353-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6353-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d6353-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6353-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d6353-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6353-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


