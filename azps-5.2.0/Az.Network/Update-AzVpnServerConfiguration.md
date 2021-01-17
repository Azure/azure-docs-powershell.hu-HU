---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336341"
---
# <span data-ttu-id="0afe7-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afe7-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="0afe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afe7-102">SYNOPSIS</span></span>
<span data-ttu-id="0afe7-103">Egy meglévő VpnServerConfiguration frissítése.</span><span class="sxs-lookup"><span data-stu-id="0afe7-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="0afe7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0afe7-104">SYNTAX</span></span>

### <span data-ttu-id="0afe7-105">ByVpnServerConfigurationNameByCertificateAuthentication (Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0afe7-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0afe7-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0afe7-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afe7-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0afe7-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0afe7-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afe7-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0afe7-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0afe7-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="0afe7-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afe7-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0afe7-114">DESCRIPTION</span></span>
<span data-ttu-id="0afe7-115">Az **Update-AzVpnServerConfiguration** parancsmaggal frissítheti a meglévő VpnServerConfigurationt különböző VpnProtocols, VpnAuthenticationTypes, IpsecPolicies és a kijelölt VPN-hitelesítéstípushoz kapcsolódó paraméterek beállításával, az ügyfélnek a "Point to site connectivity" követelménye szerint.</span><span class="sxs-lookup"><span data-stu-id="0afe7-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="0afe7-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0afe7-116">EXAMPLES</span></span>

### <span data-ttu-id="0afe7-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="0afe7-117">Example 1</span></span>
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

<span data-ttu-id="0afe7-118">A fenti parancs frissíti a meglévő VpnServerConfigurationt VpnProtocol IkeV2-ként.</span><span class="sxs-lookup"><span data-stu-id="0afe7-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="0afe7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0afe7-119">PARAMETERS</span></span>

### <span data-ttu-id="0afe7-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="0afe7-120">-AadAudience</span></span>
<span data-ttu-id="0afe7-121">AAD-közönség P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="0afe7-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="0afe7-122">-AadIssuer</span></span>
<span data-ttu-id="0afe7-123">AAD kibocsátója a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="0afe7-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="0afe7-124">-AadTenant</span></span>
<span data-ttu-id="0afe7-125">AAD-bérlő p2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="0afe7-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0afe7-126">-AsJob</span></span>
<span data-ttu-id="0afe7-127">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0afe7-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0afe7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afe7-128">-DefaultProfile</span></span>
<span data-ttu-id="0afe7-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0afe7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afe7-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0afe7-130">-InputObject</span></span>
<span data-ttu-id="0afe7-131">A vpn server configuration object to be modified</span><span class="sxs-lookup"><span data-stu-id="0afe7-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-132">-Name</span><span class="sxs-lookup"><span data-stu-id="0afe7-132">-Name</span></span>
<span data-ttu-id="0afe7-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0afe7-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-134">-SugarClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0afe7-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="0afe7-135">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="0afe7-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-136">-ServerAddress</span><span class="sxs-lookup"><span data-stu-id="0afe7-136">-RadiusServerAddress</span></span>
<span data-ttu-id="0afe7-137">A P2S külső sugarú kiszolgálójának címe.</span><span class="sxs-lookup"><span data-stu-id="0afe7-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-138">-Sugárkiszolgáló-lista</span><span class="sxs-lookup"><span data-stu-id="0afe7-138">-RadiusServerList</span></span>
<span data-ttu-id="0afe7-139">P2S Külső több sugárkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="0afe7-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-140">-ServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0afe7-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="0afe7-141">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="0afe7-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-142">-ServerSecret</span><span class="sxs-lookup"><span data-stu-id="0afe7-142">-RadiusServerSecret</span></span>
<span data-ttu-id="0afe7-143">P2S Külső sugár kiszolgálói titkos.</span><span class="sxs-lookup"><span data-stu-id="0afe7-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afe7-144">-ResourceGroupName</span></span>
<span data-ttu-id="0afe7-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0afe7-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0afe7-146">-ResourceId</span></span>
<span data-ttu-id="0afe7-147">A vpn-kiszolgáló konfigurációjának Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="0afe7-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="0afe7-148">-Tag</span></span>
<span data-ttu-id="0afe7-149">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="0afe7-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0afe7-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="0afe7-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="0afe7-151">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="0afe7-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="0afe7-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="0afe7-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="0afe7-153">A VpnServerConfiguration IPSec-házirendeinek listája.</span><span class="sxs-lookup"><span data-stu-id="0afe7-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="0afe7-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0afe7-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="0afe7-155">A vpnClientCertificates to be revoked files's paths</span><span class="sxs-lookup"><span data-stu-id="0afe7-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0afe7-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="0afe7-157">A VpnClientRootCertificates to be added files's paths listája</span><span class="sxs-lookup"><span data-stu-id="0afe7-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afe7-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="0afe7-158">-VpnProtocol</span></span>
<span data-ttu-id="0afe7-159">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="0afe7-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="0afe7-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0afe7-160">-Confirm</span></span>
<span data-ttu-id="0afe7-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0afe7-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afe7-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afe7-162">-WhatIf</span></span>
<span data-ttu-id="0afe7-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0afe7-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afe7-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0afe7-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afe7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afe7-165">CommonParameters</span></span>
<span data-ttu-id="0afe7-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afe7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afe7-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0afe7-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afe7-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0afe7-168">INPUTS</span></span>

### <span data-ttu-id="0afe7-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afe7-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="0afe7-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="0afe7-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="0afe7-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0afe7-171">OUTPUTS</span></span>

### <span data-ttu-id="0afe7-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afe7-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="0afe7-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0afe7-173">NOTES</span></span>

## <span data-ttu-id="0afe7-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0afe7-174">RELATED LINKS</span></span>
