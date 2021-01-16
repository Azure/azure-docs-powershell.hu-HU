---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345137"
---
# <span data-ttu-id="c315e-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c315e-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="c315e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c315e-102">SYNOPSIS</span></span>
<span data-ttu-id="c315e-103">Hozzon létre egy új VpnServerConfigurationt a ponttal való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="c315e-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="c315e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c315e-104">SYNTAX</span></span>

### <span data-ttu-id="c315e-105">ByVpnServerConfigurationNameByCertificateAuthentication (Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c315e-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c315e-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="c315e-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c315e-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="c315e-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c315e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c315e-108">DESCRIPTION</span></span>
<span data-ttu-id="c315e-109">A **New-AzVpnServerConfiguration** parancsmaggal új VpnServerConfigurationt hozhat létre különböző VpnProtocols, VpnAuthenticationTypes, IpsecPolicies és a kijelölt VPN-hitelesítéstípushoz kapcsolódó paraméterek beállításához az ügyfélnek a "Point to site connectivity" követelménye szerint.</span><span class="sxs-lookup"><span data-stu-id="c315e-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="c315e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c315e-110">EXAMPLES</span></span>

### <span data-ttu-id="c315e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c315e-111">Example 1</span></span>
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

<span data-ttu-id="c315e-112">A fenti parancs létrehoz egy új VpnServerConfigurationt Tanúsítványként VpnAuthenticationType-val.</span><span class="sxs-lookup"><span data-stu-id="c315e-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="c315e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c315e-113">Example 2</span></span>

<span data-ttu-id="c315e-114">Hozzon létre egy új VpnServerConfigurationt a ponttal való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="c315e-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="c315e-115">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="c315e-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="c315e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c315e-116">PARAMETERS</span></span>

### <span data-ttu-id="c315e-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="c315e-117">-AadAudience</span></span>
<span data-ttu-id="c315e-118">AAD-közönség P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="c315e-118">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c315e-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="c315e-119">-AadIssuer</span></span>
<span data-ttu-id="c315e-120">AAD kibocsátója a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="c315e-120">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c315e-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="c315e-121">-AadTenant</span></span>
<span data-ttu-id="c315e-122">AAD-bérlő p2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="c315e-122">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c315e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c315e-123">-AsJob</span></span>
<span data-ttu-id="c315e-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c315e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c315e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c315e-125">-DefaultProfile</span></span>
<span data-ttu-id="c315e-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c315e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c315e-127">-Location</span><span class="sxs-lookup"><span data-stu-id="c315e-127">-Location</span></span>
<span data-ttu-id="c315e-128">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c315e-128">The resource location.</span></span>

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

### <span data-ttu-id="c315e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c315e-129">-Name</span></span>
<span data-ttu-id="c315e-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c315e-130">The resource name.</span></span>

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

### <span data-ttu-id="c315e-131">-SugarClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c315e-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="c315e-132">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="c315e-132">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="c315e-133">-ServerAddress</span><span class="sxs-lookup"><span data-stu-id="c315e-133">-RadiusServerAddress</span></span>
<span data-ttu-id="c315e-134">A P2S külső sugarú kiszolgálójának címe.</span><span class="sxs-lookup"><span data-stu-id="c315e-134">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="c315e-135">-Sugárkiszolgáló-lista</span><span class="sxs-lookup"><span data-stu-id="c315e-135">-RadiusServerList</span></span>
<span data-ttu-id="c315e-136">P2S Külső több sugárkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="c315e-136">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="c315e-137">-ServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c315e-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="c315e-138">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="c315e-138">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="c315e-139">-ServerSecret</span><span class="sxs-lookup"><span data-stu-id="c315e-139">-RadiusServerSecret</span></span>
<span data-ttu-id="c315e-140">P2S Külső sugár kiszolgálói titkos.</span><span class="sxs-lookup"><span data-stu-id="c315e-140">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="c315e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c315e-141">-ResourceGroupName</span></span>
<span data-ttu-id="c315e-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c315e-142">The resource group name.</span></span>

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

### <span data-ttu-id="c315e-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="c315e-143">-Tag</span></span>
<span data-ttu-id="c315e-144">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="c315e-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c315e-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c315e-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="c315e-146">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="c315e-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c315e-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c315e-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c315e-148">A VpnServerConfiguration IPSec-házirendeinek listája.</span><span class="sxs-lookup"><span data-stu-id="c315e-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="c315e-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c315e-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="c315e-150">A vpnClientCertificates to be revoked files's paths</span><span class="sxs-lookup"><span data-stu-id="c315e-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="c315e-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c315e-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="c315e-152">A VpnClientRootCertificates to be added files's paths listája</span><span class="sxs-lookup"><span data-stu-id="c315e-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="c315e-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="c315e-153">-VpnProtocol</span></span>
<span data-ttu-id="c315e-154">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="c315e-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c315e-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c315e-155">-Confirm</span></span>
<span data-ttu-id="c315e-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c315e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c315e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c315e-157">-WhatIf</span></span>
<span data-ttu-id="c315e-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c315e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c315e-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c315e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c315e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c315e-160">CommonParameters</span></span>
<span data-ttu-id="c315e-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c315e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c315e-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c315e-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c315e-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c315e-163">INPUTS</span></span>

### <span data-ttu-id="c315e-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="c315e-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="c315e-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c315e-165">OUTPUTS</span></span>

### <span data-ttu-id="c315e-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c315e-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="c315e-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c315e-167">NOTES</span></span>

## <span data-ttu-id="c315e-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c315e-168">RELATED LINKS</span></span>
