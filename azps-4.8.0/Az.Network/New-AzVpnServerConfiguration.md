---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184800"
---
# <span data-ttu-id="07af7-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="07af7-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="07af7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07af7-102">SYNOPSIS</span></span>
<span data-ttu-id="07af7-103">Hozzon létre egy új VpnServerConfiguration a webhely-kapcsolat pontra.</span><span class="sxs-lookup"><span data-stu-id="07af7-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="07af7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07af7-104">SYNTAX</span></span>

### <span data-ttu-id="07af7-105">ByVpnServerConfigurationNameByCertificateAuthentication (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07af7-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07af7-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="07af7-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07af7-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="07af7-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07af7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="07af7-108">DESCRIPTION</span></span>
<span data-ttu-id="07af7-109">A **New-AzVpnServerConfiguration** parancsmag segítségével új VpnServerConfiguration hozhat létre különböző VpnProtocols, VpnAuthenticationTypes és IpsecPolicies, valamint beállíthatja a kijelölt VPN-hitelesítési típust a kapcsolódó paraméterekkel, mint az ügyfélnek a webhelyhez való kapcsolódást előfeltétele.</span><span class="sxs-lookup"><span data-stu-id="07af7-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="07af7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="07af7-110">EXAMPLES</span></span>

### <span data-ttu-id="07af7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07af7-111">Example 1</span></span>
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

<span data-ttu-id="07af7-112">A fenti parancs új VpnServerConfiguration hoz létre a VpnAuthenticationType tanúsítványként.</span><span class="sxs-lookup"><span data-stu-id="07af7-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="07af7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="07af7-113">Example 2</span></span>

<span data-ttu-id="07af7-114">Hozzon létre egy új VpnServerConfiguration a webhely-kapcsolat pontra.</span><span class="sxs-lookup"><span data-stu-id="07af7-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="07af7-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="07af7-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="07af7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07af7-116">PARAMETERS</span></span>

### <span data-ttu-id="07af7-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="07af7-117">-AadAudience</span></span>
<span data-ttu-id="07af7-118">AAD-közönség P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="07af7-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="07af7-119">-AadIssuer</span></span>
<span data-ttu-id="07af7-120">AAD a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="07af7-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="07af7-121">-AadTenant</span></span>
<span data-ttu-id="07af7-122">AAD bérlői P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="07af7-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07af7-123">-AsJob</span></span>
<span data-ttu-id="07af7-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="07af7-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07af7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07af7-125">-DefaultProfile</span></span>
<span data-ttu-id="07af7-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07af7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07af7-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="07af7-127">-Location</span></span>
<span data-ttu-id="07af7-128">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="07af7-128">The resource location.</span></span>

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

### <span data-ttu-id="07af7-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07af7-129">-Name</span></span>
<span data-ttu-id="07af7-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="07af7-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="07af7-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="07af7-132">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="07af7-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="07af7-133">-RadiusServerAddress</span></span>
<span data-ttu-id="07af7-134">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="07af7-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="07af7-135">-RadiusServerList</span></span>
<span data-ttu-id="07af7-136">P2S külső több RADIUS-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="07af7-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="07af7-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="07af7-138">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="07af7-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="07af7-139">-RadiusServerSecret</span></span>
<span data-ttu-id="07af7-140">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="07af7-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07af7-141">-ResourceGroupName</span></span>
<span data-ttu-id="07af7-142">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="07af7-142">The resource group name.</span></span>

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

### <span data-ttu-id="07af7-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="07af7-143">-Tag</span></span>
<span data-ttu-id="07af7-144">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="07af7-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="07af7-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="07af7-146">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="07af7-146">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="07af7-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="07af7-148">Az VpnServerConfiguration-hoz szükséges IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="07af7-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="07af7-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="07af7-150">A visszavonni kívánt fájlok elérési VpnClientCertificates listája</span><span class="sxs-lookup"><span data-stu-id="07af7-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="07af7-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="07af7-152">A VpnClientRootCertificates hozzáadni kívánt fájlok listája</span><span class="sxs-lookup"><span data-stu-id="07af7-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="07af7-153">-VpnProtocol</span></span>
<span data-ttu-id="07af7-154">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="07af7-154">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07af7-155">-Confirm</span></span>
<span data-ttu-id="07af7-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07af7-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07af7-157">-WhatIf</span></span>
<span data-ttu-id="07af7-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07af7-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07af7-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07af7-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07af7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07af7-160">CommonParameters</span></span>
<span data-ttu-id="07af7-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07af7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07af7-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07af7-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07af7-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07af7-163">INPUTS</span></span>

### <span data-ttu-id="07af7-164">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="07af7-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="07af7-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07af7-165">OUTPUTS</span></span>

### <span data-ttu-id="07af7-166">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="07af7-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="07af7-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07af7-167">NOTES</span></span>

## <span data-ttu-id="07af7-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07af7-168">RELATED LINKS</span></span>
