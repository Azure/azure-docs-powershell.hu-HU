---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468825"
---
# <span data-ttu-id="b6716-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b6716-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="b6716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6716-102">SYNOPSIS</span></span>
<span data-ttu-id="b6716-103">Frissíti egy alkalmazás-átjáró háttér-HTTP-beállításait.</span><span class="sxs-lookup"><span data-stu-id="b6716-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="b6716-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6716-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6716-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6716-105">DESCRIPTION</span></span>
<span data-ttu-id="b6716-106">A Set-AzApplicationGatewayBackendHttpSetting parancsmag frissíti az Azure-alkalmazásátjárók HÁTTÉR-átvitele (HTTP) beállításait.</span><span class="sxs-lookup"><span data-stu-id="b6716-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="b6716-107">A háttér-HTTP-beállításokat a rendszer a készlet összes háttérkiszolgálója esetén alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="b6716-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="b6716-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6716-108">EXAMPLES</span></span>

### <span data-ttu-id="b6716-109">1. példa: Az alkalmazásátjárók háttér-HTTP-beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="b6716-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="b6716-110">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="b6716-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b6716-111">A második parancs frissíti az alkalmazás átjárójának HTTP-beállításait a $AppGw változóban a 88-as port, a HTTP protokoll használatára, és engedélyezi a cookie-alapú affinitást.</span><span class="sxs-lookup"><span data-stu-id="b6716-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="b6716-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6716-112">PARAMETERS</span></span>

### <span data-ttu-id="b6716-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="b6716-113">-AffinityCookieName</span></span>
<span data-ttu-id="b6716-114">Az affinity cookie-hoz használható cookie-név</span><span class="sxs-lookup"><span data-stu-id="b6716-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="b6716-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6716-115">-ApplicationGateway</span></span>
<span data-ttu-id="b6716-116">Egy olyan alkalmazás-átjáróobjektumot ad meg, amellyel ez a parancsmag háttér-HTTP-beállításokat társít.</span><span class="sxs-lookup"><span data-stu-id="b6716-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="b6716-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="b6716-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="b6716-118">Az alkalmazás-átjáró hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6716-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="b6716-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b6716-119">-ConnectionDraining</span></span>
<span data-ttu-id="b6716-120">A háttérként megadott http-beállítások erőforrás kapcsolatának kiürítését.</span><span class="sxs-lookup"><span data-stu-id="b6716-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="b6716-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="b6716-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="b6716-122">Azt adja meg, hogy engedélyezve vagy letiltva legyen-e a cookie-alapú affinitás a háttérkiszolgáló-készletben.</span><span class="sxs-lookup"><span data-stu-id="b6716-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="b6716-123">A paraméter elfogadható értékei: Letiltva vagy Engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="b6716-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="b6716-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6716-124">-DefaultProfile</span></span>
<span data-ttu-id="b6716-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6716-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6716-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="b6716-126">-HostName</span></span>
<span data-ttu-id="b6716-127">Beállítja a háttérkiszolgálókra küldendő állomásfejlécet.</span><span class="sxs-lookup"><span data-stu-id="b6716-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="b6716-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b6716-128">-Name</span></span>
<span data-ttu-id="b6716-129">A háttér HTTP-beállítások objektumának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6716-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="b6716-130">-Path</span><span class="sxs-lookup"><span data-stu-id="b6716-130">-Path</span></span>
<span data-ttu-id="b6716-131">Az összes HTTP-kérelem előtagjaként használt elérési út.</span><span class="sxs-lookup"><span data-stu-id="b6716-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="b6716-132">Ha ehhez a paraméterhez nem ad meg értéket, akkor az elérési út nem lesz előtaggal megadva.</span><span class="sxs-lookup"><span data-stu-id="b6716-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="b6716-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="b6716-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="b6716-134">Jelölje meg, ha az állomásfejlécet a háttérkiszolgáló állomásnevében kell kivetni.</span><span class="sxs-lookup"><span data-stu-id="b6716-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="b6716-135">-Port</span><span class="sxs-lookup"><span data-stu-id="b6716-135">-Port</span></span>
<span data-ttu-id="b6716-136">A háttérkiszolgáló-készlet minden egyes kiszolgálójához használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6716-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="b6716-137">– Sivad</span><span class="sxs-lookup"><span data-stu-id="b6716-137">-Probe</span></span>
<span data-ttu-id="b6716-138">A háttér HTTP-beállításaihoz társítni kell egy 100 000 000 000 000 000(000)t.</span><span class="sxs-lookup"><span data-stu-id="b6716-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="b6716-139">-AzId-et</span><span class="sxs-lookup"><span data-stu-id="b6716-139">-ProbeId</span></span>
<span data-ttu-id="b6716-140">A háttér HTTP-beállításaihoz társítni megfelelő házirend azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b6716-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="b6716-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b6716-141">-Protocol</span></span>
<span data-ttu-id="b6716-142">Az alkalmazás átjárója és a háttérkiszolgálók közötti kommunikációhoz használt protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6716-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="b6716-143">A paraméter elfogadható értékei: Http és Https.</span><span class="sxs-lookup"><span data-stu-id="b6716-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="b6716-144">Ez a paraméter megkülönbözteti a kis- és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="b6716-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="b6716-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="b6716-145">-RequestTimeout</span></span>
<span data-ttu-id="b6716-146">A kérés időkorrekta-értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6716-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="b6716-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b6716-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="b6716-148">Az alkalmazás átjárója megbízható főtanúsítványok</span><span class="sxs-lookup"><span data-stu-id="b6716-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="b6716-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6716-149">CommonParameters</span></span>
<span data-ttu-id="b6716-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6716-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6716-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6716-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6716-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6716-152">INPUTS</span></span>

### <span data-ttu-id="b6716-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6716-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6716-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6716-154">OUTPUTS</span></span>

### <span data-ttu-id="b6716-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6716-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6716-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6716-156">NOTES</span></span>

## <span data-ttu-id="b6716-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6716-157">RELATED LINKS</span></span>

[<span data-ttu-id="b6716-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b6716-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="b6716-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b6716-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="b6716-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b6716-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="b6716-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b6716-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

