---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 014309ceb54b1d16b2a55c97b03887deaf4ef281
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837522"
---
# <span data-ttu-id="5d75d-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5d75d-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="5d75d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d75d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d75d-103">Back-end HTTP-beállítást hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5d75d-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="5d75d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d75d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d75d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d75d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d75d-106">Az New-AzApplicationGatewayBackendHttpSetting parancsmag az alkalmazás-átjárók back-end HTTP-beállításait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5d75d-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="5d75d-107">A back-end HTTP-beállítások a készlet minden back-end kiszolgálójára érvényesek.</span><span class="sxs-lookup"><span data-stu-id="5d75d-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="5d75d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5d75d-108">EXAMPLES</span></span>

### <span data-ttu-id="5d75d-109">Példa 1: a back-end HTTP-beállításainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="5d75d-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="5d75d-110">Ez a parancs a Setting01-on a 80-on tárolt back-end HTTP-beállításokat a HTTP protokoll használatával, a cookie-alapú affinitás letiltásával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5d75d-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="5d75d-111">A beállítások a $Setting változóban találhatók.</span><span class="sxs-lookup"><span data-stu-id="5d75d-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="5d75d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d75d-112">PARAMETERS</span></span>

### <span data-ttu-id="5d75d-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="5d75d-113">-AffinityCookieName</span></span>
<span data-ttu-id="5d75d-114">Az affinitáshoz használt cookie-név</span><span class="sxs-lookup"><span data-stu-id="5d75d-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="5d75d-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="5d75d-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="5d75d-116">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d75d-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="5d75d-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5d75d-117">-ConnectionDraining</span></span>
<span data-ttu-id="5d75d-118">A backend http Settings erőforrás kapcsolatának kiürítése</span><span class="sxs-lookup"><span data-stu-id="5d75d-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="5d75d-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="5d75d-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="5d75d-120">Azt adja meg, hogy engedélyezve van-e a cookie-alapú affinitás a back-end Server-készletben.</span><span class="sxs-lookup"><span data-stu-id="5d75d-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="5d75d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d75d-121">-DefaultProfile</span></span>
<span data-ttu-id="5d75d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d75d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d75d-123">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="5d75d-123">-HostName</span></span>
<span data-ttu-id="5d75d-124">Beállítja az állomásfejléc-ot, amelyet a backend-kiszolgálókra kell elküldeni.</span><span class="sxs-lookup"><span data-stu-id="5d75d-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="5d75d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d75d-125">-Name</span></span>
<span data-ttu-id="5d75d-126">A parancsmag által létrehozott back-end HTTP-beállítások nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d75d-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5d75d-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="5d75d-127">-Path</span></span>
<span data-ttu-id="5d75d-128">Az elérési út, amelyet az összes HTTP-kéréshez előtagként kell használni.</span><span class="sxs-lookup"><span data-stu-id="5d75d-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="5d75d-129">Ha a paraméterhez nincs megadva érték, akkor a program nem fogja előre rögzíteni az elérési utat.</span><span class="sxs-lookup"><span data-stu-id="5d75d-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="5d75d-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="5d75d-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="5d75d-131">Megjelölés ha az állomás fejlécét a backend-kiszolgáló állomásnevét kell választani.</span><span class="sxs-lookup"><span data-stu-id="5d75d-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="5d75d-132">-Port</span><span class="sxs-lookup"><span data-stu-id="5d75d-132">-Port</span></span>
<span data-ttu-id="5d75d-133">A back-end Server-készlet portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d75d-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="5d75d-134">-Szonda</span><span class="sxs-lookup"><span data-stu-id="5d75d-134">-Probe</span></span>
<span data-ttu-id="5d75d-135">A back-end Server-készlettel társítani kívánt szondát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d75d-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="5d75d-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="5d75d-136">-ProbeId</span></span>
<span data-ttu-id="5d75d-137">Annak a szondának az AZONOSÍTÓját adja meg, amely a back-end Server-készlettel társítva van.</span><span class="sxs-lookup"><span data-stu-id="5d75d-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="5d75d-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5d75d-138">-Protocol</span></span>
<span data-ttu-id="5d75d-139">Meghatározza az alkalmazás átjárója és a back-end-kiszolgálók közötti kommunikációhoz használandó protokollt.</span><span class="sxs-lookup"><span data-stu-id="5d75d-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="5d75d-140">A paraméter elfogadható értékei a következők: http és HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5d75d-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="5d75d-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="5d75d-141">-RequestTimeout</span></span>
<span data-ttu-id="5d75d-142">A kérés időtúllépési értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d75d-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="5d75d-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5d75d-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="5d75d-144">Az Application Gateway megbízható legfelső szintű tanúsítványai</span><span class="sxs-lookup"><span data-stu-id="5d75d-144">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="5d75d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d75d-145">CommonParameters</span></span>
<span data-ttu-id="5d75d-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d75d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d75d-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d75d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d75d-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d75d-148">INPUTS</span></span>

### <span data-ttu-id="5d75d-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d75d-149">None</span></span>

## <span data-ttu-id="5d75d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d75d-150">OUTPUTS</span></span>

### <span data-ttu-id="5d75d-151">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5d75d-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="5d75d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d75d-152">NOTES</span></span>

## <span data-ttu-id="5d75d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d75d-153">RELATED LINKS</span></span>

[<span data-ttu-id="5d75d-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5d75d-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5d75d-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5d75d-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5d75d-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5d75d-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5d75d-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5d75d-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

