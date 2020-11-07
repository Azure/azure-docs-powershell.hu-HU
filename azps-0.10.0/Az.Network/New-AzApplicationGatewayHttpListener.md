---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841410"
---
# <span data-ttu-id="84bce-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="84bce-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="84bce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84bce-102">SYNOPSIS</span></span>
<span data-ttu-id="84bce-103">HTTP-figyelőt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="84bce-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="84bce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84bce-104">SYNTAX</span></span>

### <span data-ttu-id="84bce-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="84bce-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84bce-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="84bce-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84bce-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="84bce-107">DESCRIPTION</span></span>
<span data-ttu-id="84bce-108">A **New-AzApplicationGatewayHttpListener** parancsmag létrehoz egy http-figyelőt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="84bce-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="84bce-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84bce-109">EXAMPLES</span></span>

### <span data-ttu-id="84bce-110">Példa 1: HTTP-figyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="84bce-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="84bce-111">Ez a parancs létrehoz egy Listener01 nevű HTTP-figyelőt, és az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84bce-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="84bce-112">2. példa: HTTP-figyelő létrehozása SSL-lel</span><span class="sxs-lookup"><span data-stu-id="84bce-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="84bce-113">Ez a parancs létrehoz egy SSL-tehermentesítést használó HTTP-figyelőt, és megadja az SSL-tanúsítványt a $SSLCert 01 változóban.</span><span class="sxs-lookup"><span data-stu-id="84bce-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="84bce-114">A parancs az eredményt az $Listener nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="84bce-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="84bce-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84bce-115">PARAMETERS</span></span>

### <span data-ttu-id="84bce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bce-116">-DefaultProfile</span></span>
<span data-ttu-id="84bce-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84bce-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84bce-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="84bce-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="84bce-119">A HTTP-figyelő előtér IP-konfigurációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84bce-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="84bce-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="84bce-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="84bce-121">A HTTP-figyelő előtér-IP-konfigurációjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84bce-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="84bce-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="84bce-122">-FrontendPort</span></span>
<span data-ttu-id="84bce-123">A HTTP-figyelő előtér-portját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84bce-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="84bce-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="84bce-124">-FrontendPortId</span></span>
<span data-ttu-id="84bce-125">A HTTP-figyelőhöz tartozó előtér-objektum AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84bce-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="84bce-126">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="84bce-126">-HostName</span></span>
<span data-ttu-id="84bce-127">Az alkalmazás-átjáró HTTP-figyelő állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84bce-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="84bce-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84bce-128">-Name</span></span>
<span data-ttu-id="84bce-129">Megadja annak a HTTP-figyelőnek a nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="84bce-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="84bce-130">-Protocol</span><span class="sxs-lookup"><span data-stu-id="84bce-130">-Protocol</span></span>
<span data-ttu-id="84bce-131">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="84bce-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="84bce-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="84bce-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="84bce-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="84bce-133">-SslCertificate</span></span>
<span data-ttu-id="84bce-134">A HTTP-figyelő SSL-tanúsítvány objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84bce-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="84bce-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="84bce-135">-SslCertificateId</span></span>
<span data-ttu-id="84bce-136">Az SSL-tanúsítvány AZONOSÍTÓját adja meg a HTTP-figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="84bce-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="84bce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bce-137">CommonParameters</span></span>
<span data-ttu-id="84bce-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84bce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bce-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84bce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bce-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84bce-140">INPUTS</span></span>

### <span data-ttu-id="84bce-141">System. String</span><span class="sxs-lookup"><span data-stu-id="84bce-141">System.String</span></span>

## <span data-ttu-id="84bce-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84bce-142">OUTPUTS</span></span>

### <span data-ttu-id="84bce-143">Microsoft. Azure. commands. Network. models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="84bce-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="84bce-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84bce-144">NOTES</span></span>

## <span data-ttu-id="84bce-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84bce-145">RELATED LINKS</span></span>

[<span data-ttu-id="84bce-146">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="84bce-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="84bce-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="84bce-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="84bce-148">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="84bce-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="84bce-149">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="84bce-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


