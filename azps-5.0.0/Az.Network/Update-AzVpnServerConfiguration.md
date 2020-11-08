---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185939"
---
# <span data-ttu-id="1e02f-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e02f-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="1e02f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e02f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e02f-103">Frissít egy meglévő VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e02f-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="1e02f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e02f-104">SYNTAX</span></span>

### <span data-ttu-id="1e02f-105">ByVpnServerConfigurationNameByCertificateAuthentication (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e02f-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e02f-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e02f-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e02f-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e02f-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e02f-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e02f-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e02f-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e02f-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="1e02f-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e02f-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e02f-114">DESCRIPTION</span></span>
<span data-ttu-id="1e02f-115">Az **Update-AzVpnServerConfiguration** parancsmag segítségével frissítheti a meglévő VpnServerConfiguration különböző VpnProtocols, VpnAuthenticationTypes, IpsecPolicies, és beállíthatja a kijelölt VPN-hitelesítési típusokat, mint az ügyfélnek a webhelyhez való kapcsolódási követelménye által előírt paramétereket.</span><span class="sxs-lookup"><span data-stu-id="1e02f-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="1e02f-116">Példák</span><span class="sxs-lookup"><span data-stu-id="1e02f-116">EXAMPLES</span></span>

### <span data-ttu-id="1e02f-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e02f-117">Example 1</span></span>
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

<span data-ttu-id="1e02f-118">A fenti parancs frissíti egy meglévő VpnServerConfiguration a VpnProtocol a IkeV2.</span><span class="sxs-lookup"><span data-stu-id="1e02f-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="1e02f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e02f-119">PARAMETERS</span></span>

### <span data-ttu-id="1e02f-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="1e02f-120">-AadAudience</span></span>
<span data-ttu-id="1e02f-121">AAD-közönség P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="1e02f-121">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="1e02f-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="1e02f-122">-AadIssuer</span></span>
<span data-ttu-id="1e02f-123">AAD a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="1e02f-123">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="1e02f-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="1e02f-124">-AadTenant</span></span>
<span data-ttu-id="1e02f-125">AAD bérlői P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="1e02f-125">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="1e02f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e02f-126">-AsJob</span></span>
<span data-ttu-id="1e02f-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1e02f-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e02f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e02f-128">-DefaultProfile</span></span>
<span data-ttu-id="1e02f-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e02f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e02f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e02f-130">-InputObject</span></span>
<span data-ttu-id="1e02f-131">A módosítani kívánt VPN-kiszolgáló konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="1e02f-131">The vpn server configuration object to be modified</span></span>

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

### <span data-ttu-id="1e02f-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e02f-132">-Name</span></span>
<span data-ttu-id="1e02f-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1e02f-133">The resource name.</span></span>

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

### <span data-ttu-id="1e02f-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e02f-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="1e02f-135">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="1e02f-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="1e02f-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1e02f-136">-RadiusServerAddress</span></span>
<span data-ttu-id="1e02f-137">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="1e02f-137">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="1e02f-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="1e02f-138">-RadiusServerList</span></span>
<span data-ttu-id="1e02f-139">P2S külső több RADIUS-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="1e02f-139">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="1e02f-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e02f-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="1e02f-141">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="1e02f-141">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="1e02f-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1e02f-142">-RadiusServerSecret</span></span>
<span data-ttu-id="1e02f-143">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="1e02f-143">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="1e02f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e02f-144">-ResourceGroupName</span></span>
<span data-ttu-id="1e02f-145">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e02f-145">The resource group name.</span></span>

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

### <span data-ttu-id="1e02f-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e02f-146">-ResourceId</span></span>
<span data-ttu-id="1e02f-147">A VPN-kiszolgáló konfigurációjának Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="1e02f-147">The Azure resource ID for the vpn server configuration.</span></span>

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

### <span data-ttu-id="1e02f-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="1e02f-148">-Tag</span></span>
<span data-ttu-id="1e02f-149">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1e02f-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1e02f-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1e02f-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="1e02f-151">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="1e02f-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1e02f-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1e02f-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="1e02f-153">Az VpnServerConfiguration-hoz szükséges IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="1e02f-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="1e02f-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e02f-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="1e02f-155">A visszavonni kívánt fájlok elérési VpnClientCertificates listája</span><span class="sxs-lookup"><span data-stu-id="1e02f-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="1e02f-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="1e02f-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="1e02f-157">A VpnClientRootCertificates hozzáadni kívánt fájlok listája</span><span class="sxs-lookup"><span data-stu-id="1e02f-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="1e02f-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="1e02f-158">-VpnProtocol</span></span>
<span data-ttu-id="1e02f-159">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="1e02f-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="1e02f-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e02f-160">-Confirm</span></span>
<span data-ttu-id="1e02f-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e02f-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e02f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e02f-162">-WhatIf</span></span>
<span data-ttu-id="1e02f-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e02f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e02f-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e02f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e02f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e02f-165">CommonParameters</span></span>
<span data-ttu-id="1e02f-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e02f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e02f-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e02f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e02f-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e02f-168">INPUTS</span></span>

### <span data-ttu-id="1e02f-169">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e02f-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="1e02f-170">System. String Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="1e02f-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="1e02f-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e02f-171">OUTPUTS</span></span>

### <span data-ttu-id="1e02f-172">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e02f-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="1e02f-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e02f-173">NOTES</span></span>

## <span data-ttu-id="1e02f-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e02f-174">RELATED LINKS</span></span>