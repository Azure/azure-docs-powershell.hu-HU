---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194706"
---
# <span data-ttu-id="e4209-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e4209-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="e4209-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4209-102">SYNOPSIS</span></span>
<span data-ttu-id="e4209-103">Kusto-fürtöt hozhat létre vagy frissíthet.</span><span class="sxs-lookup"><span data-stu-id="e4209-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="e4209-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4209-104">SYNTAX</span></span>

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

## <span data-ttu-id="e4209-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4209-105">DESCRIPTION</span></span>
<span data-ttu-id="e4209-106">Kusto-fürtöt hozhat létre vagy frissíthet.</span><span class="sxs-lookup"><span data-stu-id="e4209-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="e4209-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4209-107">EXAMPLES</span></span>

### <span data-ttu-id="e4209-108">Példa 1: új Kusto-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="e4209-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e4209-109">A fenti parancs létrehoz egy új Kusto-fürtöt, az "testnewkustocluster" nevű erőforráscsoport "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="e4209-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="e4209-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4209-110">PARAMETERS</span></span>

### <span data-ttu-id="e4209-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4209-111">-AsJob</span></span>
<span data-ttu-id="e4209-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="e4209-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e4209-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4209-113">-DefaultProfile</span></span>
<span data-ttu-id="e4209-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4209-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4209-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e4209-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="e4209-116">Logikai érték, amely azt jelzi, hogy a fürt lemezei titkosítottak-e.</span><span class="sxs-lookup"><span data-stu-id="e4209-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="e4209-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="e4209-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="e4209-118">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a dupla titkosítás.</span><span class="sxs-lookup"><span data-stu-id="e4209-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="e4209-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="e4209-119">-EnablePurge</span></span>
<span data-ttu-id="e4209-120">Logikai érték, amely azt jelzi, hogy engedélyezve vannak-e a végleges törlési műveletek.</span><span class="sxs-lookup"><span data-stu-id="e4209-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="e4209-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="e4209-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="e4209-122">Logikai érték, amely azt jelzi, hogy engedélyezve van-e az adatfolyam lenyelése.</span><span class="sxs-lookup"><span data-stu-id="e4209-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="e4209-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e4209-123">-IdentityType</span></span>
<span data-ttu-id="e4209-124">Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="e4209-124">The identity type.</span></span>

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

### <span data-ttu-id="e4209-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e4209-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="e4209-126">A Kusto-fürthöz társított felhasználói identitások listája.</span><span class="sxs-lookup"><span data-stu-id="e4209-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="e4209-127">A felhasználó személyazonosságát ismertető szótár fő hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="e4209-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="e4209-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="e4209-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="e4209-129">A Key Vault-kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="e4209-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="e4209-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e4209-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="e4209-131">A kulcs-pince URI-ja.</span><span class="sxs-lookup"><span data-stu-id="e4209-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="e4209-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e4209-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="e4209-133">A Key Vault-kulcs verziószáma.</span><span class="sxs-lookup"><span data-stu-id="e4209-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="e4209-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="e4209-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="e4209-135">A nyelvi kiterjesztések listája.</span><span class="sxs-lookup"><span data-stu-id="e4209-135">The list of language extensions.</span></span>
<span data-ttu-id="e4209-136">A kivitelezéshez tekintse meg a LANGUAGEEXTENSIONVALUE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e4209-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4209-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="e4209-137">-Location</span></span>
<span data-ttu-id="e4209-138">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="e4209-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="e4209-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4209-139">-Name</span></span>
<span data-ttu-id="e4209-140">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e4209-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e4209-141">-Várva</span><span class="sxs-lookup"><span data-stu-id="e4209-141">-NoWait</span></span>
<span data-ttu-id="e4209-142">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="e4209-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4209-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="e4209-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="e4209-144">Logikai érték, amely azt jelzi, hogy az optimalizált méretezési funkció engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="e4209-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="e4209-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="e4209-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="e4209-146">A megengedett maximális előfordulások száma</span><span class="sxs-lookup"><span data-stu-id="e4209-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="e4209-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="e4209-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="e4209-148">A megengedett minimális előfordulások száma</span><span class="sxs-lookup"><span data-stu-id="e4209-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="e4209-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="e4209-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="e4209-150">A sablon által definiált verzió (például 1).</span><span class="sxs-lookup"><span data-stu-id="e4209-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="e4209-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4209-151">-ResourceGroupName</span></span>
<span data-ttu-id="e4209-152">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4209-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e4209-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e4209-153">-SkuCapacity</span></span>
<span data-ttu-id="e4209-154">A fürt példányainak száma.</span><span class="sxs-lookup"><span data-stu-id="e4209-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="e4209-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e4209-155">-SkuName</span></span>
<span data-ttu-id="e4209-156">SKU neve.</span><span class="sxs-lookup"><span data-stu-id="e4209-156">SKU name.</span></span>

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

### <span data-ttu-id="e4209-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e4209-157">-SkuTier</span></span>
<span data-ttu-id="e4209-158">SKU Tier (SKU)</span><span class="sxs-lookup"><span data-stu-id="e4209-158">SKU tier.</span></span>

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

### <span data-ttu-id="e4209-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4209-159">-SubscriptionId</span></span>
<span data-ttu-id="e4209-160">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e4209-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4209-161">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e4209-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4209-162">-Címke</span><span class="sxs-lookup"><span data-stu-id="e4209-162">-Tag</span></span>
<span data-ttu-id="e4209-163">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="e4209-163">Resource tags.</span></span>

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

### <span data-ttu-id="e4209-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="e4209-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="e4209-165">A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="e4209-165">The cluster's external tenants.</span></span>
<span data-ttu-id="e4209-166">A kivitelezéshez tekintse meg a TRUSTEDEXTERNALTENANT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e4209-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4209-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="e4209-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="e4209-168">Az adatkezelési szolgáltatás nyilvános IP-címe erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e4209-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="e4209-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="e4209-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="e4209-170">A motor szolgáltatás nyilvános IP-címe erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e4209-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="e4209-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="e4209-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="e4209-172">Az alhálózati erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e4209-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="e4209-173">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="e4209-173">-Zone</span></span>
<span data-ttu-id="e4209-174">A fürt elérhetőségi zónái.</span><span class="sxs-lookup"><span data-stu-id="e4209-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="e4209-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4209-175">-Confirm</span></span>
<span data-ttu-id="e4209-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4209-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4209-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4209-177">-WhatIf</span></span>
<span data-ttu-id="e4209-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4209-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4209-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4209-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4209-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4209-180">CommonParameters</span></span>
<span data-ttu-id="e4209-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4209-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4209-182">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4209-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4209-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4209-183">INPUTS</span></span>

## <span data-ttu-id="e4209-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4209-184">OUTPUTS</span></span>

### <span data-ttu-id="e4209-185">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="e4209-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="e4209-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4209-186">NOTES</span></span>

<span data-ttu-id="e4209-187">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e4209-187">ALIASES</span></span>

<span data-ttu-id="e4209-188">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e4209-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4209-189">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e4209-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4209-190">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e4209-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4209-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: a nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="e4209-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="e4209-192">`[Name <LanguageExtensionName?>]`: A nyelvi kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="e4209-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="e4209-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: a klaszter külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="e4209-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="e4209-194">`[Value <String>]`: A külső bérlőt képviselő GUID azonosító.</span><span class="sxs-lookup"><span data-stu-id="e4209-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="e4209-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4209-195">RELATED LINKS</span></span>

