---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184959"
---
# <span data-ttu-id="78619-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="78619-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="78619-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78619-102">SYNOPSIS</span></span>
<span data-ttu-id="78619-103">Engedélyezze a HTTPS protokollt egy egyéni tartományhoz az első ajtó által felügyelt tanúsítvány segítségével, vagy használja az Azure Key Vault saját tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="78619-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="78619-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78619-104">SYNTAX</span></span>

### <span data-ttu-id="78619-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78619-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78619-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="78619-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78619-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78619-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78619-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="78619-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78619-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78619-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78619-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="78619-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78619-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="78619-111">DESCRIPTION</span></span>
<span data-ttu-id="78619-112">Az **enable-AzFrontDoorCustomDomainHttps** lehetővé teszi a https használatát egy egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="78619-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="78619-113">Példák</span><span class="sxs-lookup"><span data-stu-id="78619-113">EXAMPLES</span></span>

### <span data-ttu-id="78619-114">1. példa: engedélyezze a HTTPS protokollt egy egyéni tartományhoz, amelyen a FrontDoorName és a ResourceGroupName használható a bejárati ajtóval felügyelt tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="78619-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="78619-115">HTTPS engedélyezése egy egyéni tartományhoz: "frontendpointname1-Custom-XYZ", amely a bejárati ajtó "frontdoor1", az "resourcegroup1" erőforráscsoport "" az első ajtó felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="78619-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="78619-116">2. példa: engedélyezze a HTTPS protokollt egy egyéni tartományhoz, amelyen a FrontDoorName és a ResourceGroupName saját tanúsítvánnyal rendelkezik a kulcskezelő szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="78619-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="78619-117">HTTPS engedélyezése egy egyéni tartományhoz: "frontendpointname1-Custom-XYZ", amely a bejárati ajtó "frontdoor1", az "resourcegroup1" erőforráscsoport "" az első ajtó felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="78619-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="78619-118">3. példa: engedélyezze a HTTPS protokollt egy egyéni tartományhoz a PSFrontendEndpoint objektummal az első ajtó által felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="78619-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="78619-119">Engedélyezze a HTTPS protokollt egy egyéni tartományhoz a PSFrontendEndpoint objektummal az első ajtó által felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="78619-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="78619-120">Példa 4: a HTTPS engedélyezése egyéni tartományhoz erőforrás-azonosítóval az első ajtó által felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="78619-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="78619-121">HTTPS engedélyezése egyéni tartományhoz: "frontendpointname1-Custom-XYZ" az erőforrás-azonosítóval $resourceId a bejárati ajtót felügyelt tanúsítvány használatával.</span><span class="sxs-lookup"><span data-stu-id="78619-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="78619-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78619-122">PARAMETERS</span></span>

### <span data-ttu-id="78619-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78619-123">-DefaultProfile</span></span>
<span data-ttu-id="78619-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78619-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78619-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="78619-125">-FrontDoorName</span></span>
<span data-ttu-id="78619-126">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="78619-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="78619-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="78619-127">-FrontendEndpointName</span></span>
<span data-ttu-id="78619-128">A frontend végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="78619-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="78619-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78619-129">-InputObject</span></span>
<span data-ttu-id="78619-130">A frontend végpont objektum a frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="78619-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="78619-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="78619-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="78619-132">Az ügyfeleknek a bejárati ajtóval való SSL-kézfogás létesítéséhez szükséges minimális TLS-verzió.</span><span class="sxs-lookup"><span data-stu-id="78619-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="78619-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78619-133">-ResourceGroupName</span></span>
<span data-ttu-id="78619-134">Az az erőforráscsoport, amelyhez az első ajtó tartozik.</span><span class="sxs-lookup"><span data-stu-id="78619-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="78619-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78619-135">-ResourceId</span></span>
<span data-ttu-id="78619-136">A https engedélyezése a bejárati ajtó végpontjának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="78619-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="78619-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="78619-137">-SecretName</span></span>
<span data-ttu-id="78619-138">A teljes tanúsítvány (PFX) teljes tanúsítványát képviselő kulcs-Vault-titok neve</span><span class="sxs-lookup"><span data-stu-id="78619-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="78619-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="78619-139">-SecretVersion</span></span>
<span data-ttu-id="78619-140">A teljes tanúsítvány (PFX) teljes tanúsítványát jelképező kulcsfájl-titok verziója.</span><span class="sxs-lookup"><span data-stu-id="78619-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="78619-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="78619-141">-VaultId</span></span>
<span data-ttu-id="78619-142">Az SSL-tanúsítványt tartalmazó fő pince-azonosító</span><span class="sxs-lookup"><span data-stu-id="78619-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="78619-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78619-143">-Confirm</span></span>
<span data-ttu-id="78619-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78619-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78619-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78619-145">-WhatIf</span></span>
<span data-ttu-id="78619-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78619-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78619-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78619-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78619-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78619-148">CommonParameters</span></span>
<span data-ttu-id="78619-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78619-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78619-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78619-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78619-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78619-151">INPUTS</span></span>

### <span data-ttu-id="78619-152">System. String</span><span class="sxs-lookup"><span data-stu-id="78619-152">System.String</span></span>
## <span data-ttu-id="78619-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78619-153">OUTPUTS</span></span>

### <span data-ttu-id="78619-154">Microsoft. Azure. Command. FrontDoor. models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="78619-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="78619-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78619-155">NOTES</span></span>

## <span data-ttu-id="78619-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78619-156">RELATED LINKS</span></span>
