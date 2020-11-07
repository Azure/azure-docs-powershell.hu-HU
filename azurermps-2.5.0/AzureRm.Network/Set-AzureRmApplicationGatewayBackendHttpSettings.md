---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: c20faf9ca89892d952d553d0f85cfa28b90ac590
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849098"
---
# <span data-ttu-id="0169d-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0169d-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0169d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0169d-102">SYNOPSIS</span></span>
<span data-ttu-id="0169d-103">Az alkalmazás-átjárók végfelhasználói HTTP-beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="0169d-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0169d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0169d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0169d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0169d-105">DESCRIPTION</span></span>
<span data-ttu-id="0169d-106">A Set-AzureRmApplicationGatewayBackendHttpSettings parancsmag frissíti az Azure-alkalmazások átjárójának HTTP-beállításait.</span><span class="sxs-lookup"><span data-stu-id="0169d-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="0169d-107">A back-end HTTP-beállítások a készlet minden back-end kiszolgálójára érvényesek.</span><span class="sxs-lookup"><span data-stu-id="0169d-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="0169d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0169d-108">EXAMPLES</span></span>

### <span data-ttu-id="0169d-109">Példa 1: az alkalmazás-átjárók back-end HTTP-beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="0169d-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="0169d-110">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0169d-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0169d-111">A második parancs frissíti a $AppGw változóban lévő alkalmazás-átjáró HTTP-beállításait a 88-as port, a HTTP-protokoll és a cookie-alapú affinitás használatához.</span><span class="sxs-lookup"><span data-stu-id="0169d-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="0169d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0169d-112">PARAMETERS</span></span>

### <span data-ttu-id="0169d-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="0169d-113">-AffinityCookieName</span></span>
<span data-ttu-id="0169d-114">Az affinitáshoz használt cookie-név</span><span class="sxs-lookup"><span data-stu-id="0169d-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="0169d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0169d-115">-ApplicationGateway</span></span>
<span data-ttu-id="0169d-116">Itt adhatja meg azt az alkalmazásobjektum-objektumot, amelynek a parancsmagja a back-end HTTP-beállításait társítja.</span><span class="sxs-lookup"><span data-stu-id="0169d-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="0169d-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="0169d-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="0169d-118">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0169d-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="0169d-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0169d-119">-ConnectionDraining</span></span>
<span data-ttu-id="0169d-120">A backend http Settings erőforrás kapcsolatának kiürítése</span><span class="sxs-lookup"><span data-stu-id="0169d-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="0169d-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="0169d-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="0169d-122">Azt adja meg, hogy engedélyezve van-e a cookie-alapú affinitás a backend Server-készlethez, vagy le legyen tiltva.</span><span class="sxs-lookup"><span data-stu-id="0169d-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="0169d-123">A paraméter elfogadható értékei a következők: letiltva vagy engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="0169d-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="0169d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0169d-124">-DefaultProfile</span></span>
<span data-ttu-id="0169d-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0169d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0169d-126">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="0169d-126">-HostName</span></span>
<span data-ttu-id="0169d-127">Beállítja az állomásfejléc-ot, amelyet a backend-kiszolgálókra kell elküldeni.</span><span class="sxs-lookup"><span data-stu-id="0169d-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="0169d-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0169d-128">-Name</span></span>
<span data-ttu-id="0169d-129">A back-end HTTP Settings objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0169d-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="0169d-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0169d-130">-Path</span></span>
<span data-ttu-id="0169d-131">Az elérési út, amelyet az összes HTTP-kéréshez előtagként kell használni.</span><span class="sxs-lookup"><span data-stu-id="0169d-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="0169d-132">Ha a paraméterhez nincs megadva érték, akkor a program nem fogja előre rögzíteni az elérési utat.</span><span class="sxs-lookup"><span data-stu-id="0169d-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="0169d-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="0169d-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="0169d-134">Megjelölés ha az állomás fejlécét a backend-kiszolgáló állomásnevét kell választani.</span><span class="sxs-lookup"><span data-stu-id="0169d-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="0169d-135">-Port</span><span class="sxs-lookup"><span data-stu-id="0169d-135">-Port</span></span>
<span data-ttu-id="0169d-136">Megadja, hogy melyik portot használja az egyes kiszolgálók a back-end Server-készletben.</span><span class="sxs-lookup"><span data-stu-id="0169d-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="0169d-137">-Szonda</span><span class="sxs-lookup"><span data-stu-id="0169d-137">-Probe</span></span>
<span data-ttu-id="0169d-138">A back-end HTTP-beállításaival társítani kívánt szondát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0169d-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="0169d-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="0169d-139">-ProbeEnabled</span></span>
<span data-ttu-id="0169d-140">Megjelölés ha a szonda engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="0169d-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="0169d-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="0169d-141">-ProbeId</span></span>
<span data-ttu-id="0169d-142">Annak a szondanak az AZONOSÍTÓját adja meg, amely a back-end HTTP-beállításaihoz társítva van.</span><span class="sxs-lookup"><span data-stu-id="0169d-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="0169d-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0169d-143">-Protocol</span></span>
<span data-ttu-id="0169d-144">Az Application Gateway és a back-end-kiszolgálók közötti kommunikációhoz használandó protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0169d-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="0169d-145">A paraméter elfogadható értékei a következők: http és HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0169d-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="0169d-146">Ez a paraméter megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="0169d-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="0169d-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="0169d-147">-RequestTimeout</span></span>
<span data-ttu-id="0169d-148">A kérés időtúllépési értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0169d-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="0169d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0169d-149">CommonParameters</span></span>
<span data-ttu-id="0169d-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0169d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0169d-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0169d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0169d-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0169d-152">INPUTS</span></span>

### <span data-ttu-id="0169d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0169d-153">System.String</span></span>

## <span data-ttu-id="0169d-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0169d-154">OUTPUTS</span></span>

### <span data-ttu-id="0169d-155">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0169d-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0169d-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0169d-156">NOTES</span></span>

## <span data-ttu-id="0169d-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0169d-157">RELATED LINKS</span></span>

[<span data-ttu-id="0169d-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0169d-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0169d-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0169d-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0169d-160">Új – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0169d-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0169d-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0169d-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

