---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: f4c4ccdce719b3593968f0429d5e02936d052cc4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849602"
---
# <span data-ttu-id="9fe89-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9fe89-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9fe89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fe89-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe89-103">Az alkalmazások átjárójának back-end HTTP-beállításait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9fe89-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fe89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fe89-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fe89-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fe89-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe89-106">Az New-AzureRmApplicationGatewayBackendHttpSettings parancsmag az alkalmazás-átjárók back-end HTTP-beállításait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9fe89-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="9fe89-107">A back-end HTTP-beállítások a készlet minden back-end kiszolgálójára érvényesek.</span><span class="sxs-lookup"><span data-stu-id="9fe89-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="9fe89-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9fe89-108">EXAMPLES</span></span>

### <span data-ttu-id="9fe89-109">Példa 1: a back-end HTTP-beállításainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fe89-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="9fe89-110">Ez a parancs a Setting01-on a 80-on tárolt back-end HTTP-beállításokat a HTTP protokoll használatával, a cookie-alapú affinitás letiltásával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9fe89-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="9fe89-111">A beállítások a $Setting változóban találhatók.</span><span class="sxs-lookup"><span data-stu-id="9fe89-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="9fe89-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fe89-112">PARAMETERS</span></span>

### <span data-ttu-id="9fe89-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="9fe89-113">-AffinityCookieName</span></span>
<span data-ttu-id="9fe89-114">Az affinitáshoz használt cookie-név</span><span class="sxs-lookup"><span data-stu-id="9fe89-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="9fe89-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="9fe89-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="9fe89-116">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fe89-116">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9fe89-117">-ConnectionDraining</span></span>
<span data-ttu-id="9fe89-118">A backend http Settings erőforrás kapcsolatának kiürítése</span><span class="sxs-lookup"><span data-stu-id="9fe89-118">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="9fe89-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="9fe89-120">Azt adja meg, hogy engedélyezve van-e a cookie-alapú affinitás a back-end Server-készletben.</span><span class="sxs-lookup"><span data-stu-id="9fe89-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe89-121">-DefaultProfile</span></span>
<span data-ttu-id="9fe89-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fe89-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fe89-123">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="9fe89-123">-HostName</span></span>
<span data-ttu-id="9fe89-124">Beállítja az állomásfejléc-ot, amelyet a backend-kiszolgálókra kell elküldeni.</span><span class="sxs-lookup"><span data-stu-id="9fe89-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="9fe89-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9fe89-125">-Name</span></span>
<span data-ttu-id="9fe89-126">A parancsmag által létrehozott back-end HTTP-beállítások nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fe89-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9fe89-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9fe89-127">-Path</span></span>
<span data-ttu-id="9fe89-128">Az elérési út, amelyet az összes HTTP-kéréshez előtagként kell használni.</span><span class="sxs-lookup"><span data-stu-id="9fe89-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="9fe89-129">Ha a paraméterhez nincs megadva érték, akkor a program nem fogja előre rögzíteni az elérési utat.</span><span class="sxs-lookup"><span data-stu-id="9fe89-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="9fe89-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="9fe89-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="9fe89-131">Megjelölés ha az állomás fejlécét a backend-kiszolgáló állomásnevét kell választani.</span><span class="sxs-lookup"><span data-stu-id="9fe89-131">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-132">-Port</span><span class="sxs-lookup"><span data-stu-id="9fe89-132">-Port</span></span>
<span data-ttu-id="9fe89-133">A back-end Server-készlet portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fe89-133">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-134">-Szonda</span><span class="sxs-lookup"><span data-stu-id="9fe89-134">-Probe</span></span>
<span data-ttu-id="9fe89-135">A back-end Server-készlettel társítani kívánt szondát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fe89-135">Specifies a probe to associate with the back-end server pool.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fe89-136">-ProbeEnabled</span></span>
<span data-ttu-id="9fe89-137">Megjelölés ha a szonda engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="9fe89-137">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="9fe89-138">-ProbeId</span></span>
<span data-ttu-id="9fe89-139">Annak a szondának az AZONOSÍTÓját adja meg, amely a back-end Server-készlettel társítva van.</span><span class="sxs-lookup"><span data-stu-id="9fe89-139">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="9fe89-140">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9fe89-140">-Protocol</span></span>
<span data-ttu-id="9fe89-141">Meghatározza az alkalmazás átjárója és a back-end-kiszolgálók közötti kommunikációhoz használandó protokollt.</span><span class="sxs-lookup"><span data-stu-id="9fe89-141">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="9fe89-142">A paraméter elfogadható értékei a következők: http és HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9fe89-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="9fe89-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="9fe89-143">-RequestTimeout</span></span>
<span data-ttu-id="9fe89-144">A kérés időtúllépési értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fe89-144">Specifies a request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe89-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe89-145">CommonParameters</span></span>
<span data-ttu-id="9fe89-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fe89-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe89-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe89-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe89-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fe89-148">INPUTS</span></span>

### <span data-ttu-id="9fe89-149">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe89-149">System.String</span></span>

## <span data-ttu-id="9fe89-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fe89-150">OUTPUTS</span></span>

### <span data-ttu-id="9fe89-151">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9fe89-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9fe89-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fe89-152">NOTES</span></span>

## <span data-ttu-id="9fe89-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fe89-153">RELATED LINKS</span></span>

[<span data-ttu-id="9fe89-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9fe89-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="9fe89-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9fe89-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="9fe89-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9fe89-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="9fe89-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9fe89-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

