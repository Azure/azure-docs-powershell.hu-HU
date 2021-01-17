---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354377"
---
# <span data-ttu-id="a1a1d-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="a1a1d-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="a1a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a1d-103">Engedélyezze a HTTPS-t egy egyéni tartományhoz a Front Door felügyelt tanúsítványával vagy az Azure key vaultból származó saját tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="a1a1d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1a1d-104">SYNTAX</span></span>

### <span data-ttu-id="a1a1d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1a1d-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a1d-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1a1d-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1a1d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1a1d-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a1d-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1a1d-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a1d-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1a1d-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1a1d-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1a1d-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1a1d-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1a1d-111">DESCRIPTION</span></span>
<span data-ttu-id="a1a1d-112">Az **Enable-AzFrontDoorCustomDomainHttps** engedélyezi a HTTPS-t egy egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="a1a1d-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1a1d-113">EXAMPLES</span></span>

### <span data-ttu-id="a1a1d-114">1. példa: A FrontDoorName és a ResourceGroupName protokollt használó egyéni tartomány HTTPS-címének engedélyezése a Front Door felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="a1a1d-115">Engedélyezze a HTTPS-t egy egyéni tartományhoz (frontendpointname1-custom-xyz) az "resourcegroup1" erőforráscsoport "frontdoor1" nevű erőforráscsoportban a Front Door felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="a1a1d-116">2. példa: A HTTPS engedélyezése a FrontDoorName és a ResourceGroupName egyéni tartományhoz saját tanúsítvány használatával a kulcstárolóban.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="a1a1d-117">Engedélyezze a HTTPS-t egy egyéni tartományhoz (frontendpointname1-custom-xyz) az "resourcegroup1" erőforráscsoport "frontdoor1" nevű erőforráscsoportban a Front Door felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="a1a1d-118">3. példa: A HTTPS engedélyezése egyéni tartományhoz a PSFrontendEndpoint-objektummal a Front Door felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="a1a1d-119">Engedélyezze a HTTPS-t a PSFrontendEndpoint-objektum egyéni tartományához a Front Door felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="a1a1d-120">4. példa: A HTTPS engedélyezése egy olyan egyéni tartományhoz, amely a Front Door felügyelt tanúsítványt használja erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="a1a1d-121">Engedélyezze a HTTPS-t a "frontendpointname1-custom-xyz" egyéni tartományhoz úgy, hogy $resourceId a Front Door felügyelt tanúsítványt használva.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="a1a1d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1a1d-122">PARAMETERS</span></span>

### <span data-ttu-id="a1a1d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a1d-123">-DefaultProfile</span></span>
<span data-ttu-id="a1a1d-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1a1d-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a1a1d-125">-FrontDoorName</span></span>
<span data-ttu-id="a1a1d-126">A front door neve.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="a1a1d-127">-FrontendEndpointName</span></span>
<span data-ttu-id="a1a1d-128">Frontend endpoint name.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1a1d-129">-InputObject</span></span>
<span data-ttu-id="a1a1d-130">A frissítend frontend végpontobjektum.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a1a1d-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="a1a1d-132">Az SSL-kézbeszélőnek a Front Door segítségével való létesítéséhez az ügyfelek által megkövetelt minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="a1a1d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1a1d-133">-ResourceGroupName</span></span>
<span data-ttu-id="a1a1d-134">Az az erőforráscsoport, amelyhez a Front Door tartozik.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1a1d-135">-ResourceId</span></span>
<span data-ttu-id="a1a1d-136">A front door végpont erőforrás-azonosítója a https engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="a1a1d-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="a1a1d-137">-SecretName</span></span>
<span data-ttu-id="a1a1d-138">A pfX teljes tanúsítványt képviselő kulcstároló-titkos kulcs neve</span><span class="sxs-lookup"><span data-stu-id="a1a1d-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="a1a1d-139">-SecretVersion</span></span>
<span data-ttu-id="a1a1d-140">A kulcstároló titkos verziója, amely a teljes PFX tanúsítványt képviseli</span><span class="sxs-lookup"><span data-stu-id="a1a1d-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a1a1d-141">-VaultId</span></span>
<span data-ttu-id="a1a1d-142">Az SSL-tanúsítványt tartalmazó kulcstároló azonosítója</span><span class="sxs-lookup"><span data-stu-id="a1a1d-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1a1d-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1a1d-143">-Confirm</span></span>
<span data-ttu-id="a1a1d-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a1d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a1d-145">-WhatIf</span></span>
<span data-ttu-id="a1a1d-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1a1d-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a1d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a1d-148">CommonParameters</span></span>
<span data-ttu-id="a1a1d-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a1d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a1d-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1a1d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a1d-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1a1d-151">INPUTS</span></span>

### <span data-ttu-id="a1a1d-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a1a1d-152">System.String</span></span>
## <span data-ttu-id="a1a1d-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1a1d-153">OUTPUTS</span></span>

### <span data-ttu-id="a1a1d-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1a1d-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="a1a1d-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1a1d-155">NOTES</span></span>

## <span data-ttu-id="a1a1d-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1a1d-156">RELATED LINKS</span></span>
