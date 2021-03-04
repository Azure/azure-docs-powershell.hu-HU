---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: f093a9f3a30ce1e46c08790d355689fdd9399c79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934793"
---
# <span data-ttu-id="6c255-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c255-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="6c255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c255-102">SYNOPSIS</span></span>
<span data-ttu-id="6c255-103">Hozzon létre egy új VpnServerConfigurationt a ponttal való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="6c255-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="6c255-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c255-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c255-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c255-105">DESCRIPTION</span></span>
<span data-ttu-id="6c255-106">A **New-AzVpnServerConfiguration** parancsmaggal új VpnServerConfigurationt hozhat létre különböző VpnProtocols, VpnAuthenticationTypes, IpsecPolicies és a kijelölt VPN-hitelesítéstípushoz kapcsolódó paraméterek beállításához az ügyfélnek a "Point to site connectivity" követelménye szerint.</span><span class="sxs-lookup"><span data-stu-id="6c255-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="6c255-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c255-107">EXAMPLES</span></span>

### <span data-ttu-id="6c255-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6c255-108">Example 1</span></span>
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

<span data-ttu-id="6c255-109">A fenti parancs létrehoz egy új VpnServerConfigurationt Tanúsítványként VpnAuthenticationType-val.</span><span class="sxs-lookup"><span data-stu-id="6c255-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="6c255-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="6c255-110">Example 2</span></span>

<span data-ttu-id="6c255-111">Hozzon létre egy új VpnServerConfigurationt a ponttal való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="6c255-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="6c255-112">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="6c255-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="6c255-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c255-113">PARAMETERS</span></span>

### <span data-ttu-id="6c255-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="6c255-114">-AadAudience</span></span>
<span data-ttu-id="6c255-115">AAD-közönség P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="6c255-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="6c255-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="6c255-116">-AadIssuer</span></span>
<span data-ttu-id="6c255-117">AAD kibocsátója a P2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="6c255-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="6c255-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="6c255-118">-AadTenant</span></span>
<span data-ttu-id="6c255-119">AAD-bérlő p2S AAD-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="6c255-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="6c255-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c255-120">-AsJob</span></span>
<span data-ttu-id="6c255-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6c255-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c255-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c255-122">-DefaultProfile</span></span>
<span data-ttu-id="6c255-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c255-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c255-124">-Location</span><span class="sxs-lookup"><span data-stu-id="6c255-124">-Location</span></span>
<span data-ttu-id="6c255-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="6c255-125">The resource location.</span></span>

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

### <span data-ttu-id="6c255-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6c255-126">-Name</span></span>
<span data-ttu-id="6c255-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6c255-127">The resource name.</span></span>

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

### <span data-ttu-id="6c255-128">-SugarClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6c255-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="6c255-129">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="6c255-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="6c255-130">-ServerAddress</span><span class="sxs-lookup"><span data-stu-id="6c255-130">-RadiusServerAddress</span></span>
<span data-ttu-id="6c255-131">A P2S külső sugarú kiszolgálójának címe.</span><span class="sxs-lookup"><span data-stu-id="6c255-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="6c255-132">-Sugárkiszolgáló-lista</span><span class="sxs-lookup"><span data-stu-id="6c255-132">-RadiusServerList</span></span>
<span data-ttu-id="6c255-133">P2S Külső több sugárkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="6c255-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="6c255-134">-ServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6c255-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="6c255-135">A SugarClientRootCertificate fájlok elérési útvonalának listája</span><span class="sxs-lookup"><span data-stu-id="6c255-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="6c255-136">-ServerSecret</span><span class="sxs-lookup"><span data-stu-id="6c255-136">-RadiusServerSecret</span></span>
<span data-ttu-id="6c255-137">P2S Külső sugár kiszolgálói titkos.</span><span class="sxs-lookup"><span data-stu-id="6c255-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="6c255-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c255-138">-ResourceGroupName</span></span>
<span data-ttu-id="6c255-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c255-139">The resource group name.</span></span>

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

### <span data-ttu-id="6c255-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c255-140">-Tag</span></span>
<span data-ttu-id="6c255-141">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="6c255-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6c255-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="6c255-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="6c255-143">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="6c255-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="6c255-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6c255-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="6c255-145">A VpnServerConfiguration IPSec-házirendeinek listája.</span><span class="sxs-lookup"><span data-stu-id="6c255-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="6c255-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6c255-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="6c255-147">A vpnClientCertificates to be revoked files's paths</span><span class="sxs-lookup"><span data-stu-id="6c255-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="6c255-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6c255-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="6c255-149">A VpnClientRootCertificates to be added files's paths listája</span><span class="sxs-lookup"><span data-stu-id="6c255-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="6c255-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="6c255-150">-VpnProtocol</span></span>
<span data-ttu-id="6c255-151">A P2S VPN-ügyfél alagutasíték-protokolljainak listája.</span><span class="sxs-lookup"><span data-stu-id="6c255-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="6c255-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c255-152">-Confirm</span></span>
<span data-ttu-id="6c255-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6c255-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c255-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c255-154">-WhatIf</span></span>
<span data-ttu-id="6c255-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6c255-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c255-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c255-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c255-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c255-157">CommonParameters</span></span>
<span data-ttu-id="6c255-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c255-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c255-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c255-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c255-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c255-160">INPUTS</span></span>

### <span data-ttu-id="6c255-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="6c255-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="6c255-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c255-162">OUTPUTS</span></span>

### <span data-ttu-id="6c255-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c255-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="6c255-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c255-164">NOTES</span></span>

## <span data-ttu-id="6c255-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c255-165">RELATED LINKS</span></span>
