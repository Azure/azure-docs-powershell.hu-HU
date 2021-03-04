---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 3e60546992957a027dd5bbb94281e19e74e42274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930961"
---
# <span data-ttu-id="2cce1-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2cce1-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="2cce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cce1-102">SYNOPSIS</span></span>
<span data-ttu-id="2cce1-103">Új Azure tűzfal-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="2cce1-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="2cce1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2cce1-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cce1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2cce1-105">DESCRIPTION</span></span>
<span data-ttu-id="2cce1-106">A **New-AzFirewallPolicy** parancsmag létrehoz egy Azure tűzfalházi házirendet.</span><span class="sxs-lookup"><span data-stu-id="2cce1-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="2cce1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2cce1-107">EXAMPLES</span></span>

### <span data-ttu-id="2cce1-108">1. példa: 1.</span><span class="sxs-lookup"><span data-stu-id="2cce1-108">Example 1: 1.</span></span> <span data-ttu-id="2cce1-109">Üres házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="2cce1-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="2cce1-110">Ebben a példában egy Azure tűzfal-házirendet hoz létre</span><span class="sxs-lookup"><span data-stu-id="2cce1-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="2cce1-111">2. példa: 2.</span><span class="sxs-lookup"><span data-stu-id="2cce1-111">Example 2: 2.</span></span> <span data-ttu-id="2cce1-112">Üres házirend létrehozása a ThreatIntel módban</span><span class="sxs-lookup"><span data-stu-id="2cce1-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="2cce1-113">Ebben a példában egy veszélyforrás-intel módú Azure tűzfal-házirendet hoz létre</span><span class="sxs-lookup"><span data-stu-id="2cce1-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="2cce1-114">3. példa: 3.</span><span class="sxs-lookup"><span data-stu-id="2cce1-114">Example 3: 3.</span></span> <span data-ttu-id="2cce1-115">Üres házirend létrehozása a ThreatIntel Whitelist segítségével</span><span class="sxs-lookup"><span data-stu-id="2cce1-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="2cce1-116">Ez a példa létrehoz egy Azure tűzfal házirendet veszélyforrás-intel whitelistával</span><span class="sxs-lookup"><span data-stu-id="2cce1-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="2cce1-117">4. példa: 4.</span><span class="sxs-lookup"><span data-stu-id="2cce1-117">Example 4: 4.</span></span> <span data-ttu-id="2cce1-118">Házirend létrehozása a behatolás észleléséhez, az identitáshoz és az átviteli biztonsághoz</span><span class="sxs-lookup"><span data-stu-id="2cce1-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="2cce1-119">Ebben a példában egy azure tűzfal-házirendet hoz létre, amely a behúzás észlelését riasztási módban, a felhasználóhoz rendelt identitást és az átviteli biztonságot használja</span><span class="sxs-lookup"><span data-stu-id="2cce1-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="2cce1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cce1-120">PARAMETERS</span></span>

### <span data-ttu-id="2cce1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cce1-121">-AsJob</span></span>
<span data-ttu-id="2cce1-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2cce1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cce1-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="2cce1-123">-BasePolicy</span></span>
<span data-ttu-id="2cce1-124">Az alap házirend, amelytől örökölni kell</span><span class="sxs-lookup"><span data-stu-id="2cce1-124">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cce1-125">-DefaultProfile</span></span>
<span data-ttu-id="2cce1-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cce1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cce1-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="2cce1-127">-DnsSetting</span></span>
<span data-ttu-id="2cce1-128">A DNS-beállítás</span><span class="sxs-lookup"><span data-stu-id="2cce1-128">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-129">-Force</span><span class="sxs-lookup"><span data-stu-id="2cce1-129">-Force</span></span>
<span data-ttu-id="2cce1-130">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="2cce1-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2cce1-131">-Identity</span><span class="sxs-lookup"><span data-stu-id="2cce1-131">-Identity</span></span>
<span data-ttu-id="2cce1-132">Tűzfal házirend-identitás, amely a tűzfal-házirendhez lesz hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="2cce1-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="2cce1-133">-IntrusionDetection</span></span>
<span data-ttu-id="2cce1-134">A Behatolás észlelése beállítás</span><span class="sxs-lookup"><span data-stu-id="2cce1-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-135">-Location</span><span class="sxs-lookup"><span data-stu-id="2cce1-135">-Location</span></span>
<span data-ttu-id="2cce1-136">helyére.</span><span class="sxs-lookup"><span data-stu-id="2cce1-136">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2cce1-137">-Name</span></span>
<span data-ttu-id="2cce1-138">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2cce1-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cce1-139">-ResourceGroupName</span></span>
<span data-ttu-id="2cce1-140">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2cce1-140">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2cce1-141">-SkuTier</span></span>
<span data-ttu-id="2cce1-142">Tűzfal-házirend termékváltozatrétege</span><span class="sxs-lookup"><span data-stu-id="2cce1-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="2cce1-143">-Tag</span></span>
<span data-ttu-id="2cce1-144">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="2cce1-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="2cce1-145">-ThreatIntelMode</span></span>
<span data-ttu-id="2cce1-146">A veszélyforrás-felderítés műveleti módja.</span><span class="sxs-lookup"><span data-stu-id="2cce1-146">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2cce1-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="2cce1-148">The whitelist for Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="2cce1-148">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="2cce1-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="2cce1-150">A KeyVaultban tárolt "Titkos" vagy "Tanúsítvány" objektum titkos azonosítója (base-64 kódolt nem titkosított pfx)</span><span class="sxs-lookup"><span data-stu-id="2cce1-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="2cce1-151">-TransportSecurityName</span></span>
<span data-ttu-id="2cce1-152">Átviteli biztonsági név</span><span class="sxs-lookup"><span data-stu-id="2cce1-152">Transport security name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="2cce1-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="2cce1-154">Annak a felhasználónak az Erőforrásazonosítója, akihez a tűzfal-házirendhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2cce1-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cce1-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cce1-155">-Confirm</span></span>
<span data-ttu-id="2cce1-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2cce1-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cce1-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cce1-157">-WhatIf</span></span>
<span data-ttu-id="2cce1-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2cce1-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cce1-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2cce1-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cce1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cce1-160">CommonParameters</span></span>
<span data-ttu-id="2cce1-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cce1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cce1-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cce1-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cce1-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cce1-163">INPUTS</span></span>

### <span data-ttu-id="2cce1-164">System.String</span><span class="sxs-lookup"><span data-stu-id="2cce1-164">System.String</span></span>

### <span data-ttu-id="2cce1-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2cce1-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2cce1-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cce1-166">OUTPUTS</span></span>

### <span data-ttu-id="2cce1-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2cce1-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="2cce1-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2cce1-168">NOTES</span></span>

## <span data-ttu-id="2cce1-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cce1-169">RELATED LINKS</span></span>
