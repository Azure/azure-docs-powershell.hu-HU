---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 7b3d38b8f55c93c4527d92969ec64ce792bca44b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848121"
---
# <span data-ttu-id="a9870-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9870-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a9870-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9870-102">SYNOPSIS</span></span>
<span data-ttu-id="a9870-103">Az alkalmazás-átjárók HTTP-figyelését módosítja.</span><span class="sxs-lookup"><span data-stu-id="a9870-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9870-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9870-104">SYNTAX</span></span>

### <span data-ttu-id="a9870-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9870-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9870-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a9870-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9870-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9870-107">DESCRIPTION</span></span>
<span data-ttu-id="a9870-108">A **set-AzureRmApplicationGatewayHttpListener** parancsmag módosította az Azure Application ÁTJÁRÓk http-figyelőjét.</span><span class="sxs-lookup"><span data-stu-id="a9870-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a9870-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a9870-109">EXAMPLES</span></span>

### <span data-ttu-id="a9870-110">Példa 1: HTTP-figyelő beállítása</span><span class="sxs-lookup"><span data-stu-id="a9870-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="a9870-111">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9870-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a9870-112">A második parancs az átjáróhoz tartozó HTTP-figyelőt állítja be a 80 $FIP-on tárolt, az előtér-konfigurációban lévő HTTP-protokollon keresztül.</span><span class="sxs-lookup"><span data-stu-id="a9870-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="a9870-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9870-113">PARAMETERS</span></span>

### <span data-ttu-id="a9870-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9870-114">-ApplicationGateway</span></span>
<span data-ttu-id="a9870-115">Annak az alkalmazásnak az átjáróját adja meg, amelyhez ez a parancsmag társítja a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="a9870-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="a9870-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9870-116">-DefaultProfile</span></span>
<span data-ttu-id="a9870-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9870-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9870-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9870-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a9870-119">Az alkalmazás-átjáró előtér IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9870-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a9870-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a9870-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a9870-121">Az alkalmazás-átjáró előtér-IP-címének AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9870-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a9870-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a9870-122">-FrontendPort</span></span>
<span data-ttu-id="a9870-123">Az Application Gateway előtér-portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9870-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="a9870-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a9870-124">-FrontendPortId</span></span>
<span data-ttu-id="a9870-125">Az Application Gateway előtér-port AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9870-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="a9870-126">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="a9870-126">-HostName</span></span>
<span data-ttu-id="a9870-127">Azt az állomásnevet adja meg, amelyre a parancsmag a HTTP-figyelőt elküldi.</span><span class="sxs-lookup"><span data-stu-id="a9870-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="a9870-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9870-128">-Name</span></span>
<span data-ttu-id="a9870-129">A HTTP-figyelő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9870-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="a9870-130">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a9870-130">-Protocol</span></span>
<span data-ttu-id="a9870-131">A HTTP-figyelő által használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9870-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="a9870-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a9870-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9870-133">Http</span><span class="sxs-lookup"><span data-stu-id="a9870-133">Http</span></span>
- <span data-ttu-id="a9870-134">Https</span><span class="sxs-lookup"><span data-stu-id="a9870-134">Https</span></span>

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

### <span data-ttu-id="a9870-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a9870-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="a9870-136">Azt adja meg, hogy a parancsmagnak meg kell-e adni a kiszolgálónév jelzését.</span><span class="sxs-lookup"><span data-stu-id="a9870-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="a9870-137">A paraméter elfogadható értékei a következők: igaz vagy hamis.</span><span class="sxs-lookup"><span data-stu-id="a9870-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="a9870-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9870-138">-SslCertificate</span></span>
<span data-ttu-id="a9870-139">A HTTP-figyelő SSL-tanúsítványát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9870-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="a9870-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a9870-140">-SslCertificateId</span></span>
<span data-ttu-id="a9870-141">Megadja a HTTP-figyelő Secure Socket Layer (SSL) tanúsítvány-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a9870-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="a9870-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9870-142">CommonParameters</span></span>
<span data-ttu-id="a9870-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9870-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9870-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9870-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9870-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9870-145">INPUTS</span></span>

### <span data-ttu-id="a9870-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a9870-146">System.String</span></span>

## <span data-ttu-id="a9870-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9870-147">OUTPUTS</span></span>

### <span data-ttu-id="a9870-148">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9870-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a9870-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9870-149">NOTES</span></span>

## <span data-ttu-id="a9870-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9870-150">RELATED LINKS</span></span>

[<span data-ttu-id="a9870-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9870-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a9870-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9870-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a9870-153">Új – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9870-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a9870-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a9870-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


