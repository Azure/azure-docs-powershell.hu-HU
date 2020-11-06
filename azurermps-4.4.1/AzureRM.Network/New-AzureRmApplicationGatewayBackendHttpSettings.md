---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 6183b3cd61380b139bd74d676c6ab5225bf338fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499955"
---
# <span data-ttu-id="2b102-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b102-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2b102-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b102-102">SYNOPSIS</span></span>
<span data-ttu-id="2b102-103">Az alkalmazások átjárójának back-end HTTP-beállításait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b102-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b102-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b102-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b102-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b102-105">DESCRIPTION</span></span>
<span data-ttu-id="2b102-106">Az New-AzureRmApplicationGatewayBackendHttpSettings parancsmag az alkalmazás-átjárók back-end HTTP-beállításait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b102-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="2b102-107">A back-end HTTP-beállítások a készlet minden back-end kiszolgálójára érvényesek.</span><span class="sxs-lookup"><span data-stu-id="2b102-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="2b102-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2b102-108">EXAMPLES</span></span>

### <span data-ttu-id="2b102-109">Példa 1: a back-end HTTP-beállításainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="2b102-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="2b102-110">Ez a parancs a Setting01-on a 80-on tárolt back-end HTTP-beállításokat a HTTP protokoll használatával, a cookie-alapú affinitás letiltásával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b102-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="2b102-111">A beállítások a $Setting változóban találhatók.</span><span class="sxs-lookup"><span data-stu-id="2b102-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="2b102-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b102-112">PARAMETERS</span></span>

### <span data-ttu-id="2b102-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="2b102-113">-AffinityCookieName</span></span>
<span data-ttu-id="2b102-114">Az affinitáshoz használt cookie-név</span><span class="sxs-lookup"><span data-stu-id="2b102-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="2b102-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="2b102-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="2b102-116">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b102-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="2b102-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2b102-117">-ConnectionDraining</span></span>
<span data-ttu-id="2b102-118">A backend http Settings erőforrás kapcsolatának kiürítése</span><span class="sxs-lookup"><span data-stu-id="2b102-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="2b102-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="2b102-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="2b102-120">Azt adja meg, hogy engedélyezve van-e a cookie-alapú affinitás a back-end Server-készletben.</span><span class="sxs-lookup"><span data-stu-id="2b102-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="2b102-121">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="2b102-121">-HostName</span></span>
<span data-ttu-id="2b102-122">Beállítja az állomásfejléc-ot, amelyet a backend-kiszolgálókra kell elküldeni.</span><span class="sxs-lookup"><span data-stu-id="2b102-122">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="2b102-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b102-123">-Name</span></span>
<span data-ttu-id="2b102-124">A parancsmag által létrehozott back-end HTTP-beállítások nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b102-124">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2b102-125">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="2b102-125">-Path</span></span>
<span data-ttu-id="2b102-126">Az elérési út, amelyet az összes HTTP-kéréshez előtagként kell használni.</span><span class="sxs-lookup"><span data-stu-id="2b102-126">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="2b102-127">Ha a paraméterhez nincs megadva érték, akkor a program nem fogja előre rögzíteni az elérési utat.</span><span class="sxs-lookup"><span data-stu-id="2b102-127">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="2b102-128">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="2b102-128">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="2b102-129">Megjelölés ha az állomás fejlécét a backend-kiszolgáló állomásnevét kell választani.</span><span class="sxs-lookup"><span data-stu-id="2b102-129">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="2b102-130">-Port</span><span class="sxs-lookup"><span data-stu-id="2b102-130">-Port</span></span>
<span data-ttu-id="2b102-131">A back-end Server-készlet portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b102-131">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="2b102-132">-Szonda</span><span class="sxs-lookup"><span data-stu-id="2b102-132">-Probe</span></span>
<span data-ttu-id="2b102-133">A back-end Server-készlettel társítani kívánt szondát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b102-133">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="2b102-134">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="2b102-134">-ProbeEnabled</span></span>
<span data-ttu-id="2b102-135">Megjelölés ha a szonda engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2b102-135">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="2b102-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="2b102-136">-ProbeId</span></span>
<span data-ttu-id="2b102-137">Annak a szondának az AZONOSÍTÓját adja meg, amely a back-end Server-készlettel társítva van.</span><span class="sxs-lookup"><span data-stu-id="2b102-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="2b102-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2b102-138">-Protocol</span></span>
<span data-ttu-id="2b102-139">Meghatározza az alkalmazás átjárója és a back-end-kiszolgálók közötti kommunikációhoz használandó protokollt.</span><span class="sxs-lookup"><span data-stu-id="2b102-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="2b102-140">A paraméter elfogadható értékei a következők: http és HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2b102-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="2b102-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="2b102-141">-RequestTimeout</span></span>
<span data-ttu-id="2b102-142">A kérés időtúllépési értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b102-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="2b102-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b102-143">-DefaultProfile</span></span>
<span data-ttu-id="2b102-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b102-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b102-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b102-145">CommonParameters</span></span>
<span data-ttu-id="2b102-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b102-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b102-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b102-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b102-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b102-148">INPUTS</span></span>

### <span data-ttu-id="2b102-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2b102-149">System.String</span></span>

## <span data-ttu-id="2b102-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b102-150">OUTPUTS</span></span>

### <span data-ttu-id="2b102-151">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b102-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2b102-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b102-152">NOTES</span></span>

## <span data-ttu-id="2b102-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b102-153">RELATED LINKS</span></span>

[<span data-ttu-id="2b102-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b102-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="2b102-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b102-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="2b102-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b102-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="2b102-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b102-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

