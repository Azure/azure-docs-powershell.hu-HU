---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: e5bd6c612cb78d2c6d38a1484452c814ecdf714c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918337"
---
# <span data-ttu-id="bf65c-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf65c-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="bf65c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf65c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf65c-103">Egy meglévő VpnServerConfiguration frissítése.</span><span class="sxs-lookup"><span data-stu-id="bf65c-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="bf65c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bf65c-104">SYNTAX</span></span>

### <span data-ttu-id="bf65c-105">ByVpnServerConfigurationName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf65c-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf65c-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="bf65c-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf65c-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="bf65c-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf65c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bf65c-108">DESCRIPTION</span></span>
<span data-ttu-id="bf65c-109">Az **Update-AzVpnServerConfiguration** parancsmaggal frissítheti a meglévő VpnServerConfigurationt különböző VpnProtocols, VpnAuthenticationTypes, IpsecPolicies és a kijelölt VPN-hitelesítéstípushoz kapcsolódó paraméterek beállításával, az ügyfélnek a "Point to site connectivity" követelménye szerint.</span><span class="sxs-lookup"><span data-stu-id="bf65c-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="bf65c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bf65c-110">EXAMPLES</span></span>

### <span data-ttu-id="bf65c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bf65c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
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

<span data-ttu-id="bf65c-112">A fenti parancs frissíti a meglévő VpnServerConfigurationt VpnProtocol IkeV2-ként.</span><span class="sxs-lookup"><span data-stu-id="bf65c-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="bf65c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf65c-113">PARAMETERS</span></span>

### <span data-ttu-id="bf65c-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="bf65c-114">-AadAudience</span></span>
<span data-ttu-id="bf65c-115">AAD-közönség P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="bf65c-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="bf65c-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="bf65c-116">-AadIssuer</span></span>
<span data-ttu-id="bf65c-117">AAD kibocsátója a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="bf65c-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="bf65c-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="bf65c-118">-AadTenant</span></span>
<span data-ttu-id="bf65c-119">AAD-bérlő p2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="bf65c-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="bf65c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf65c-120">-AsJob</span></span>
<span data-ttu-id="bf65c-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bf65c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf65c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf65c-122">-DefaultProfile</span></span>
<span data-ttu-id="bf65c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf65c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf65c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf65c-124">-InputObject</span></span>
<span data-ttu-id="bf65c-125">A vpn server configuration object to be modified</span><span class="sxs-lookup"><span data-stu-id="bf65c-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bf65c-126">-Name</span></span>
<span data-ttu-id="bf65c-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bf65c-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-128">-SugarClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="bf65c-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="bf65c-129">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="bf65c-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-130">-ServerAddress</span><span class="sxs-lookup"><span data-stu-id="bf65c-130">-RadiusServerAddress</span></span>
<span data-ttu-id="bf65c-131">A P2S külső sugarú kiszolgálójának címe.</span><span class="sxs-lookup"><span data-stu-id="bf65c-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="bf65c-132">-Sugárkiszolgáló-lista</span><span class="sxs-lookup"><span data-stu-id="bf65c-132">-RadiusServerList</span></span>
<span data-ttu-id="bf65c-133">P2S Külső több sugárkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="bf65c-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-134">-ServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="bf65c-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="bf65c-135">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="bf65c-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-136">-ServerSecret</span><span class="sxs-lookup"><span data-stu-id="bf65c-136">-RadiusServerSecret</span></span>
<span data-ttu-id="bf65c-137">P2S Külső sugár kiszolgálói titkos.</span><span class="sxs-lookup"><span data-stu-id="bf65c-137">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf65c-138">-ResourceGroupName</span></span>
<span data-ttu-id="bf65c-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf65c-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf65c-140">-ResourceId</span></span>
<span data-ttu-id="bf65c-141">A vpn-kiszolgáló konfigurációjának Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf65c-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf65c-142">-Tag</span></span>
<span data-ttu-id="bf65c-143">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="bf65c-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bf65c-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="bf65c-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="bf65c-145">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="bf65c-145">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="bf65c-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bf65c-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="bf65c-147">A VpnServerConfiguration IPSec-házirendeinek listája.</span><span class="sxs-lookup"><span data-stu-id="bf65c-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="bf65c-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="bf65c-149">A vpnClientCertificates to be revoked files's paths</span><span class="sxs-lookup"><span data-stu-id="bf65c-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="bf65c-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="bf65c-151">A VpnClientRootCertificates to be added files's paths listája</span><span class="sxs-lookup"><span data-stu-id="bf65c-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf65c-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="bf65c-152">-VpnProtocol</span></span>
<span data-ttu-id="bf65c-153">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="bf65c-153">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="bf65c-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf65c-154">-Confirm</span></span>
<span data-ttu-id="bf65c-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bf65c-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf65c-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf65c-156">-WhatIf</span></span>
<span data-ttu-id="bf65c-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bf65c-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf65c-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf65c-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf65c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf65c-159">CommonParameters</span></span>
<span data-ttu-id="bf65c-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf65c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf65c-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf65c-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf65c-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf65c-162">INPUTS</span></span>

### <span data-ttu-id="bf65c-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf65c-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="bf65c-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="bf65c-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="bf65c-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf65c-165">OUTPUTS</span></span>

### <span data-ttu-id="bf65c-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf65c-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="bf65c-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bf65c-167">NOTES</span></span>

## <span data-ttu-id="bf65c-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf65c-168">RELATED LINKS</span></span>
