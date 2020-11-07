---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 325c4ca100bae93f88baaa9eb5c3fa6f2d3ecafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837698"
---
# <span data-ttu-id="158d4-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="158d4-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="158d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="158d4-102">SYNOPSIS</span></span>
<span data-ttu-id="158d4-103">Visszaadja a HTTP-beállításokat egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="158d4-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="158d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="158d4-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="158d4-105">DESCRIPTION</span></span>
<span data-ttu-id="158d4-106">Az Add-AzApplicationGatewayBackendHttpSetting parancsmag a HTTP-beállításokat egy alkalmazás-átjáróhoz adja vissza.</span><span class="sxs-lookup"><span data-stu-id="158d4-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="158d4-107">A back-end HTTP-beállítások a készlet minden back-end kiszolgálójára érvényesek.</span><span class="sxs-lookup"><span data-stu-id="158d4-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="158d4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="158d4-108">EXAMPLES</span></span>

### <span data-ttu-id="158d4-109">1. példa: a back-end HTTP-beállítások felvétele az alkalmazás-átjáróba</span><span class="sxs-lookup"><span data-stu-id="158d4-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="158d4-110">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja. A második parancs hozzáadja a back-end HTTP-beállításokat az alkalmazás-átjáróhoz, a portot a 88-ra, a protokollt pedig a HTTP-re, és megnevezi a beállítások Setting02.</span><span class="sxs-lookup"><span data-stu-id="158d4-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="158d4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="158d4-111">PARAMETERS</span></span>

### <span data-ttu-id="158d4-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="158d4-112">-AffinityCookieName</span></span>
<span data-ttu-id="158d4-113">Az affinitáshoz használt cookie-név</span><span class="sxs-lookup"><span data-stu-id="158d4-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="158d4-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="158d4-114">-ApplicationGateway</span></span>
<span data-ttu-id="158d4-115">Annak az alkalmazás-átjárónak a nevét adja meg, amelyhez a parancsmag hozzáadja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="158d4-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="158d4-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="158d4-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="158d4-117">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="158d4-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="158d4-118">-ConnectionDraining</span></span>
<span data-ttu-id="158d4-119">A backend http Settings erőforrás kapcsolatának kiürítése</span><span class="sxs-lookup"><span data-stu-id="158d4-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="158d4-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="158d4-121">Azt adja meg, hogy engedélyezve van-e a cookie-alapú affinitás a backend Server-készlethez, vagy le legyen tiltva.</span><span class="sxs-lookup"><span data-stu-id="158d4-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="158d4-122">A paraméter elfogadható értékei a következők: letiltva, engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="158d4-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158d4-123">-DefaultProfile</span></span>
<span data-ttu-id="158d4-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="158d4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158d4-125">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="158d4-125">-HostName</span></span>
<span data-ttu-id="158d4-126">Beállítja az állomásfejléc-ot, amelyet a backend-kiszolgálókra kell elküldeni.</span><span class="sxs-lookup"><span data-stu-id="158d4-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="158d4-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="158d4-127">-Name</span></span>
<span data-ttu-id="158d4-128">A bővítmény által hozzáadott back-end HTTP-beállítások nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="158d4-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="158d4-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="158d4-129">-Path</span></span>
<span data-ttu-id="158d4-130">Az elérési út, amelyet az összes HTTP-kéréshez előtagként kell használni.</span><span class="sxs-lookup"><span data-stu-id="158d4-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="158d4-131">Ha a paraméterhez nincs megadva érték, akkor a program nem fogja előre rögzíteni az elérési utat.</span><span class="sxs-lookup"><span data-stu-id="158d4-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="158d4-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="158d4-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="158d4-133">Megjelölés ha az állomás fejlécét a backend-kiszolgáló állomásnevét kell választani.</span><span class="sxs-lookup"><span data-stu-id="158d4-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-134">-Port</span><span class="sxs-lookup"><span data-stu-id="158d4-134">-Port</span></span>
<span data-ttu-id="158d4-135">A back-end Server-készlet portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="158d4-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-136">-Szonda</span><span class="sxs-lookup"><span data-stu-id="158d4-136">-Probe</span></span>
<span data-ttu-id="158d4-137">A back-end-kiszolgálóval társítani kívánt szondát adja meg.</span><span class="sxs-lookup"><span data-stu-id="158d4-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="158d4-138">-ProbeId</span></span>
<span data-ttu-id="158d4-139">Annak a szondának az AZONOSÍTÓját adja meg, amely a back-end-kiszolgálóval van társítva.</span><span class="sxs-lookup"><span data-stu-id="158d4-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="158d4-140">-Protocol</span><span class="sxs-lookup"><span data-stu-id="158d4-140">-Protocol</span></span>
<span data-ttu-id="158d4-141">Az alkalmazásobjektum-és a back-end-kiszolgálók közötti kapcsolat protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="158d4-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="158d4-142">A paraméter elfogadható értékei a következők: http és HTTPS.</span><span class="sxs-lookup"><span data-stu-id="158d4-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="158d4-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="158d4-143">-RequestTimeout</span></span>
<span data-ttu-id="158d4-144">A kérés időtúllépési értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="158d4-144">Specifies the request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="158d4-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="158d4-146">Az Application Gateway megbízható legfelső szintű tanúsítványai</span><span class="sxs-lookup"><span data-stu-id="158d4-146">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158d4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158d4-147">CommonParameters</span></span>
<span data-ttu-id="158d4-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="158d4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158d4-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158d4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158d4-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="158d4-150">INPUTS</span></span>

### <span data-ttu-id="158d4-151">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="158d4-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="158d4-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="158d4-152">OUTPUTS</span></span>

### <span data-ttu-id="158d4-153">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="158d4-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="158d4-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="158d4-154">NOTES</span></span>

## <span data-ttu-id="158d4-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="158d4-155">RELATED LINKS</span></span>

[<span data-ttu-id="158d4-156">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="158d4-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="158d4-157">Új – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="158d4-157">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="158d4-158">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="158d4-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="158d4-159">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="158d4-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

