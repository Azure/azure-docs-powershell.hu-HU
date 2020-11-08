---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 14f43ab66800969eb46554de898525ce8d687f5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013211"
---
# <span data-ttu-id="a8308-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8308-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a8308-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8308-102">SYNOPSIS</span></span>
<span data-ttu-id="a8308-103">Frissít egy meglévő VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a8308-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="a8308-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8308-104">SYNTAX</span></span>

### <span data-ttu-id="a8308-105">ByVpnServerConfigurationNameByCertificateAuthentication (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8308-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8308-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8308-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8308-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8308-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8308-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8308-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8308-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8308-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a8308-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8308-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8308-114">DESCRIPTION</span></span>
<span data-ttu-id="a8308-115">Az **Update-AzVpnServerConfiguration** parancsmag segítségével frissítheti a meglévő VpnServerConfiguration különböző VpnProtocols, VpnAuthenticationTypes, IpsecPolicies, és beállíthatja a kijelölt VPN-hitelesítési típusokat, mint az ügyfélnek a webhelyhez való kapcsolódási követelménye által előírt paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a8308-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a8308-116">Példák</span><span class="sxs-lookup"><span data-stu-id="a8308-116">EXAMPLES</span></span>

### <span data-ttu-id="a8308-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a8308-117">Example 1</span></span>
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

<span data-ttu-id="a8308-118">A fenti parancs frissíti egy meglévő VpnServerConfiguration a VpnProtocol a IkeV2.</span><span class="sxs-lookup"><span data-stu-id="a8308-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="a8308-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8308-119">PARAMETERS</span></span>

### <span data-ttu-id="a8308-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a8308-120">-AadAudience</span></span>
<span data-ttu-id="a8308-121">AAD-közönség P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="a8308-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="a8308-122">-AadIssuer</span></span>
<span data-ttu-id="a8308-123">AAD a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="a8308-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a8308-124">-AadTenant</span></span>
<span data-ttu-id="a8308-125">AAD bérlői P2S AAD-hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="a8308-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8308-126">-AsJob</span></span>
<span data-ttu-id="a8308-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a8308-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8308-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8308-128">-DefaultProfile</span></span>
<span data-ttu-id="a8308-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8308-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8308-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8308-130">-InputObject</span></span>
<span data-ttu-id="a8308-131">A módosítani kívánt VPN-kiszolgáló konfigurációs objektuma</span><span class="sxs-lookup"><span data-stu-id="a8308-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8308-132">-Name</span></span>
<span data-ttu-id="a8308-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a8308-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8308-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a8308-135">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="a8308-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a8308-136">-RadiusServerAddress</span></span>
<span data-ttu-id="a8308-137">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="a8308-137">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-138">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8308-138">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a8308-139">A RadiusClientRootCertificate-fájlok elérési útjának listája</span><span class="sxs-lookup"><span data-stu-id="a8308-139">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a8308-140">-RadiusServerSecret</span></span>
<span data-ttu-id="a8308-141">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="a8308-141">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8308-142">-ResourceGroupName</span></span>
<span data-ttu-id="a8308-143">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a8308-143">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8308-144">-ResourceId</span></span>
<span data-ttu-id="a8308-145">A VPN-kiszolgáló konfigurációjának Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="a8308-145">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="a8308-146">-Tag</span></span>
<span data-ttu-id="a8308-147">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a8308-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a8308-148">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a8308-148">-VpnAuthenticationType</span></span>
<span data-ttu-id="a8308-149">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="a8308-149">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a8308-150">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a8308-150">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a8308-151">Az VpnServerConfiguration-hoz szükséges IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="a8308-151">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-152">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8308-152">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a8308-153">A visszavonni kívánt fájlok elérési VpnClientCertificates listája</span><span class="sxs-lookup"><span data-stu-id="a8308-153">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-154">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a8308-154">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a8308-155">A VpnClientRootCertificates hozzáadni kívánt fájlok listája</span><span class="sxs-lookup"><span data-stu-id="a8308-155">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8308-156">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a8308-156">-VpnProtocol</span></span>
<span data-ttu-id="a8308-157">A P2S VPN-ügyfél bújtatási protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="a8308-157">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a8308-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8308-158">-Confirm</span></span>
<span data-ttu-id="a8308-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8308-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8308-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8308-160">-WhatIf</span></span>
<span data-ttu-id="a8308-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8308-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8308-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8308-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8308-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8308-163">CommonParameters</span></span>
<span data-ttu-id="a8308-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8308-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8308-165">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8308-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8308-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8308-166">INPUTS</span></span>

### <span data-ttu-id="a8308-167">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8308-167">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="a8308-168">System. String Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a8308-168">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a8308-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8308-169">OUTPUTS</span></span>

### <span data-ttu-id="a8308-170">Microsoft. Azure. commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8308-170">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a8308-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8308-171">NOTES</span></span>

## <span data-ttu-id="a8308-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8308-172">RELATED LINKS</span></span>
