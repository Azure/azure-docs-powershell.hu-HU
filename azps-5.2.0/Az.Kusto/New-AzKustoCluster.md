---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359042"
---
# <span data-ttu-id="5893b-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="5893b-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="5893b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5893b-102">SYNOPSIS</span></span>
<span data-ttu-id="5893b-103">Kusto-fürt létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="5893b-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="5893b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5893b-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5893b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5893b-105">DESCRIPTION</span></span>
<span data-ttu-id="5893b-106">Kusto-fürt létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="5893b-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="5893b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5893b-107">EXAMPLES</span></span>

### <span data-ttu-id="5893b-108">1. példa: Új Kusto-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="5893b-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="5893b-109">A fenti parancs létrehoz egy "testnewkustocluster" nevű új Kusto-fürtöt a "testrg" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="5893b-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="5893b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5893b-110">PARAMETERS</span></span>

### <span data-ttu-id="5893b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5893b-111">-AsJob</span></span>
<span data-ttu-id="5893b-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="5893b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5893b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5893b-113">-DefaultProfile</span></span>
<span data-ttu-id="5893b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5893b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5893b-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="5893b-116">Logikai érték, amely azt jelzi, hogy a fürt lemezei titkosítottak-e.</span><span class="sxs-lookup"><span data-stu-id="5893b-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="5893b-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="5893b-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="5893b-118">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a dupla titkosítás.</span><span class="sxs-lookup"><span data-stu-id="5893b-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="5893b-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="5893b-119">-EnablePurge</span></span>
<span data-ttu-id="5893b-120">Logikai érték, amely azt jelzi, hogy a véglegesen megadott műveletek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="5893b-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="5893b-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="5893b-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="5893b-122">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a folyamatos átvitel.</span><span class="sxs-lookup"><span data-stu-id="5893b-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="5893b-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5893b-123">-IdentityType</span></span>
<span data-ttu-id="5893b-124">Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="5893b-124">The identity type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5893b-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="5893b-126">A Kusto-fürthöz társított felhasználói identitások listája.</span><span class="sxs-lookup"><span data-stu-id="5893b-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="5893b-127">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="5893b-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="5893b-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="5893b-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="5893b-129">A kulcs tárolókulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="5893b-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="5893b-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="5893b-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="5893b-131">A kulcstár Uri-ja.</span><span class="sxs-lookup"><span data-stu-id="5893b-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="5893b-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="5893b-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="5893b-133">A kulcs tárolókulcsának verziója.</span><span class="sxs-lookup"><span data-stu-id="5893b-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="5893b-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="5893b-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="5893b-135">A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="5893b-135">The list of language extensions.</span></span>
<span data-ttu-id="5893b-136">A felépítéshez a LANGUAGEEXTENSIONVALUE tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="5893b-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-137">-Location</span><span class="sxs-lookup"><span data-stu-id="5893b-137">-Location</span></span>
<span data-ttu-id="5893b-138">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="5893b-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="5893b-139">-Name</span><span class="sxs-lookup"><span data-stu-id="5893b-139">-Name</span></span>
<span data-ttu-id="5893b-140">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="5893b-140">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5893b-141">-NoWait</span></span>
<span data-ttu-id="5893b-142">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="5893b-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5893b-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="5893b-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="5893b-144">Logikai érték, amely azt jelzi, hogy az optimalizált automatikusskála funkció engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="5893b-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="5893b-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="5893b-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="5893b-146">A maximálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="5893b-146">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="5893b-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="5893b-148">A minimálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="5893b-148">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="5893b-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="5893b-150">A sablon definiált verziója, például 1.</span><span class="sxs-lookup"><span data-stu-id="5893b-150">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5893b-151">-ResourceGroupName</span></span>
<span data-ttu-id="5893b-152">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5893b-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5893b-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5893b-153">-SkuCapacity</span></span>
<span data-ttu-id="5893b-154">A fürt példányainak száma.</span><span class="sxs-lookup"><span data-stu-id="5893b-154">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5893b-155">-SkuName</span></span>
<span data-ttu-id="5893b-156">Termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="5893b-156">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5893b-157">-SkuTier</span></span>
<span data-ttu-id="5893b-158">Termékváltozatréteg.</span><span class="sxs-lookup"><span data-stu-id="5893b-158">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5893b-159">-SubscriptionId</span></span>
<span data-ttu-id="5893b-160">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5893b-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5893b-161">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5893b-161">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="5893b-162">-Tag</span></span>
<span data-ttu-id="5893b-163">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="5893b-163">Resource tags.</span></span>

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

### <span data-ttu-id="5893b-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="5893b-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="5893b-165">A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="5893b-165">The cluster's external tenants.</span></span>
<span data-ttu-id="5893b-166">Ennek létrehozásáról a TRUSTEDEXTERNALTENANT tulajdonságokAT és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="5893b-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5893b-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="5893b-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="5893b-168">Adatkezelési nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5893b-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="5893b-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="5893b-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="5893b-170">A motorszolgáltatás nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5893b-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="5893b-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="5893b-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="5893b-172">Az alhálózati erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5893b-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="5893b-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="5893b-173">-Zone</span></span>
<span data-ttu-id="5893b-174">A fürt elérhetőségi zónái.</span><span class="sxs-lookup"><span data-stu-id="5893b-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="5893b-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5893b-175">-Confirm</span></span>
<span data-ttu-id="5893b-176">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5893b-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5893b-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5893b-177">-WhatIf</span></span>
<span data-ttu-id="5893b-178">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5893b-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5893b-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5893b-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5893b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5893b-180">CommonParameters</span></span>
<span data-ttu-id="5893b-181">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5893b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5893b-182">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5893b-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5893b-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5893b-183">INPUTS</span></span>

## <span data-ttu-id="5893b-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5893b-184">OUTPUTS</span></span>

### <span data-ttu-id="5893b-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span><span class="sxs-lookup"><span data-stu-id="5893b-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="5893b-186">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5893b-186">NOTES</span></span>

<span data-ttu-id="5893b-187">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5893b-187">ALIASES</span></span>

<span data-ttu-id="5893b-188">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5893b-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5893b-189">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5893b-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5893b-190">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5893b-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5893b-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="5893b-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="5893b-192">`[Name <LanguageExtensionName?>]`: A nyelvbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="5893b-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="5893b-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="5893b-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="5893b-194">`[Value <String>]`: Külső bérlő guid azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5893b-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="5893b-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5893b-195">RELATED LINKS</span></span>

