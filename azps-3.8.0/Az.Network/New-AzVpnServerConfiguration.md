---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846698"
---
# <span data-ttu-id="f8be2-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8be2-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="f8be2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8be2-102">SYNOPSIS</span></span>
<span data-ttu-id="f8be2-103">Hozzon létre egy új VpnServerConfiguration a webhely-kapcsolat pontra.</span><span class="sxs-lookup"><span data-stu-id="f8be2-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="f8be2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8be2-104">SYNTAX</span></span>

### <span data-ttu-id="f8be2-105">ByVpnServerConfigurationNameByCertificateAuthentication (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8be2-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8be2-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="f8be2-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8be2-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="f8be2-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8be2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8be2-108">DESCRIPTION</span></span>
<span data-ttu-id="f8be2-109">A **New-AzVpnServerConfiguration** parancsmag segítségével új VpnServerConfiguration hozhat létre különböző VpnProtocols, VpnAuthenticationTypes és IpsecPolicies, valamint beállíthatja a kijelölt VPN-hitelesítési típust a kapcsolódó paraméterekkel, mint az ügyfélnek a webhelyhez való kapcsolódást előfeltétele.</span><span class="sxs-lookup"><span data-stu-id="f8be2-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="f8be2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f8be2-110">EXAMPLES</span></span>

### <span data-ttu-id="f8be2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f8be2-111">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="f8be2-112">A fenti parancs új VpnServerConfiguration hoz létre a VpnAuthenticationType tanúsítványként.</span><span class="sxs-lookup"><span data-stu-id="f8be2-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="f8be2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8be2-113">PARAMETERS</span></span>

### <span data-ttu-id="f8be2-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="f8be2-114">-AadAudience</span></span>
<span data-ttu-id="f8be2-115">AAD-közönség P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="f8be2-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="f8be2-116">-AadIssuer</span></span>
<span data-ttu-id="f8be2-117">AAD a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="f8be2-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="f8be2-118">-AadTenant</span></span>
<span data-ttu-id="f8be2-119">AAD bérlői P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="f8be2-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8be2-120">-AsJob</span></span>
<span data-ttu-id="f8be2-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f8be2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8be2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8be2-122">-DefaultProfile</span></span>
<span data-ttu-id="f8be2-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8be2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="f8be2-124">-Location</span></span>
<span data-ttu-id="f8be2-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f8be2-125">The resource location.</span></span>

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

### <span data-ttu-id="f8be2-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8be2-126">-Name</span></span>
<span data-ttu-id="f8be2-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f8be2-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f8be2-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="f8be2-129">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="f8be2-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f8be2-130">-RadiusServerAddress</span></span>
<span data-ttu-id="f8be2-131">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="f8be2-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f8be2-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="f8be2-133">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="f8be2-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f8be2-134">-RadiusServerSecret</span></span>
<span data-ttu-id="f8be2-135">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="f8be2-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8be2-136">-ResourceGroupName</span></span>
<span data-ttu-id="f8be2-137">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8be2-137">The resource group name.</span></span>

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

### <span data-ttu-id="f8be2-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="f8be2-138">-Tag</span></span>
<span data-ttu-id="f8be2-139">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f8be2-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f8be2-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="f8be2-141">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="f8be2-141">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f8be2-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f8be2-143">Az VpnServerConfiguration-hoz szükséges IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="f8be2-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f8be2-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="f8be2-145">A visszavonni kívánt fájlok elérési VpnClientCertificates listája</span><span class="sxs-lookup"><span data-stu-id="f8be2-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="f8be2-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="f8be2-147">A VpnClientRootCertificates hozzáadni kívánt fájlok listája</span><span class="sxs-lookup"><span data-stu-id="f8be2-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="f8be2-148">-VpnProtocol</span></span>
<span data-ttu-id="f8be2-149">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="f8be2-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f8be2-150">-Confirm</span></span>
<span data-ttu-id="f8be2-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f8be2-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8be2-152">-WhatIf</span></span>
<span data-ttu-id="f8be2-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f8be2-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8be2-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8be2-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8be2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8be2-155">CommonParameters</span></span>
<span data-ttu-id="f8be2-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8be2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8be2-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8be2-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8be2-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8be2-158">INPUTS</span></span>

### <span data-ttu-id="f8be2-159">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="f8be2-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="f8be2-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8be2-160">OUTPUTS</span></span>

### <span data-ttu-id="f8be2-161">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8be2-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="f8be2-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8be2-162">NOTES</span></span>

## <span data-ttu-id="f8be2-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8be2-163">RELATED LINKS</span></span>
