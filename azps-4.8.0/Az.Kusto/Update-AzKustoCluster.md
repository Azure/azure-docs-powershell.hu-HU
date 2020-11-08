---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184491"
---
# <span data-ttu-id="d02b1-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d02b1-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="d02b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d02b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d02b1-103">Frissítsen egy Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="d02b1-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="d02b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d02b1-104">SYNTAX</span></span>

### <span data-ttu-id="d02b1-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d02b1-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d02b1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d02b1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d02b1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d02b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d02b1-108">Frissítsen egy Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="d02b1-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="d02b1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d02b1-109">EXAMPLES</span></span>

### <span data-ttu-id="d02b1-110">Példa 1: meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d02b1-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d02b1-111">A fenti parancs frissíti a "testnewkustocluster" Kusto-cluster "" SKU-ot a "testrg" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="d02b1-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d02b1-112">2. példa: meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d02b1-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d02b1-113">A fenti parancs frissíti a "testnewkustocluster" cluster "testrg" erőforráscsoportot az ügyfél által felügyelt kulccsal.</span><span class="sxs-lookup"><span data-stu-id="d02b1-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="d02b1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d02b1-114">PARAMETERS</span></span>

### <span data-ttu-id="d02b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d02b1-115">-AsJob</span></span>
<span data-ttu-id="d02b1-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d02b1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d02b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d02b1-117">-DefaultProfile</span></span>
<span data-ttu-id="d02b1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d02b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d02b1-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d02b1-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="d02b1-120">Logikai érték, amely azt jelzi, hogy a fürt lemezei titkosítottak-e.</span><span class="sxs-lookup"><span data-stu-id="d02b1-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="d02b1-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="d02b1-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="d02b1-122">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a dupla titkosítás.</span><span class="sxs-lookup"><span data-stu-id="d02b1-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="d02b1-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="d02b1-123">-EnablePurge</span></span>
<span data-ttu-id="d02b1-124">Logikai érték, amely azt jelzi, hogy engedélyezve vannak-e a végleges törlési műveletek.</span><span class="sxs-lookup"><span data-stu-id="d02b1-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="d02b1-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="d02b1-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="d02b1-126">Logikai érték, amely azt jelzi, hogy engedélyezve van-e az adatfolyam lenyelése.</span><span class="sxs-lookup"><span data-stu-id="d02b1-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="d02b1-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d02b1-127">-IdentityType</span></span>
<span data-ttu-id="d02b1-128">Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="d02b1-128">The identity type.</span></span>

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

### <span data-ttu-id="d02b1-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d02b1-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="d02b1-130">A Kusto-fürthöz társított felhasználói identitások listája.</span><span class="sxs-lookup"><span data-stu-id="d02b1-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="d02b1-131">A felhasználó személyazonosságát ismertető szótár fő hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="d02b1-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="d02b1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d02b1-132">-InputObject</span></span>
<span data-ttu-id="d02b1-133">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d02b1-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d02b1-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="d02b1-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="d02b1-135">A Key Vault-kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="d02b1-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d02b1-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="d02b1-137">A kulcs-pince URI-ja.</span><span class="sxs-lookup"><span data-stu-id="d02b1-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="d02b1-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d02b1-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="d02b1-139">A Key Vault-kulcs verziószáma.</span><span class="sxs-lookup"><span data-stu-id="d02b1-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="d02b1-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="d02b1-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="d02b1-141">A nyelvi kiterjesztések listája.</span><span class="sxs-lookup"><span data-stu-id="d02b1-141">The list of language extensions.</span></span>
<span data-ttu-id="d02b1-142">A kivitelezéshez tekintse meg a LANGUAGEEXTENSIONVALUE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d02b1-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d02b1-143">-Hely</span><span class="sxs-lookup"><span data-stu-id="d02b1-143">-Location</span></span>
<span data-ttu-id="d02b1-144">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d02b1-144">Resource location.</span></span>

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

### <span data-ttu-id="d02b1-145">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d02b1-145">-Name</span></span>
<span data-ttu-id="d02b1-146">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d02b1-147">-Várva</span><span class="sxs-lookup"><span data-stu-id="d02b1-147">-NoWait</span></span>
<span data-ttu-id="d02b1-148">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d02b1-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d02b1-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d02b1-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="d02b1-150">Logikai érték, amely azt jelzi, hogy az optimalizált méretezési funkció engedélyezve van-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="d02b1-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="d02b1-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="d02b1-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="d02b1-152">A megengedett maximális előfordulások száma</span><span class="sxs-lookup"><span data-stu-id="d02b1-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="d02b1-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="d02b1-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="d02b1-154">A megengedett minimális előfordulások száma</span><span class="sxs-lookup"><span data-stu-id="d02b1-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="d02b1-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="d02b1-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="d02b1-156">A sablon által definiált verzió (például 1).</span><span class="sxs-lookup"><span data-stu-id="d02b1-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="d02b1-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d02b1-157">-ResourceGroupName</span></span>
<span data-ttu-id="d02b1-158">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d02b1-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d02b1-159">-SkuCapacity</span></span>
<span data-ttu-id="d02b1-160">A fürt példányainak száma.</span><span class="sxs-lookup"><span data-stu-id="d02b1-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="d02b1-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d02b1-161">-SkuName</span></span>
<span data-ttu-id="d02b1-162">SKU neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d02b1-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d02b1-163">-SkuTier</span></span>
<span data-ttu-id="d02b1-164">SKU Tier (SKU)</span><span class="sxs-lookup"><span data-stu-id="d02b1-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d02b1-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d02b1-165">-SubscriptionId</span></span>
<span data-ttu-id="d02b1-166">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d02b1-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d02b1-167">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d02b1-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d02b1-168">-Címke</span><span class="sxs-lookup"><span data-stu-id="d02b1-168">-Tag</span></span>
<span data-ttu-id="d02b1-169">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="d02b1-169">Resource tags.</span></span>

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

### <span data-ttu-id="d02b1-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="d02b1-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="d02b1-171">A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="d02b1-171">The cluster's external tenants.</span></span>
<span data-ttu-id="d02b1-172">A kivitelezéshez tekintse meg a TRUSTEDEXTERNALTENANT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d02b1-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d02b1-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="d02b1-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="d02b1-174">Az adatkezelési szolgáltatás nyilvános IP-címe erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d02b1-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="d02b1-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="d02b1-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="d02b1-176">A motor szolgáltatás nyilvános IP-címe erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d02b1-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="d02b1-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="d02b1-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="d02b1-178">Az alhálózati erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d02b1-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="d02b1-179">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d02b1-179">-Confirm</span></span>
<span data-ttu-id="d02b1-180">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d02b1-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d02b1-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d02b1-181">-WhatIf</span></span>
<span data-ttu-id="d02b1-182">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d02b1-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d02b1-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d02b1-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d02b1-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d02b1-184">CommonParameters</span></span>
<span data-ttu-id="d02b1-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d02b1-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d02b1-186">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d02b1-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d02b1-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d02b1-187">INPUTS</span></span>

### <span data-ttu-id="d02b1-188">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d02b1-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d02b1-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d02b1-189">OUTPUTS</span></span>

### <span data-ttu-id="d02b1-190">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="d02b1-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="d02b1-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d02b1-191">NOTES</span></span>

<span data-ttu-id="d02b1-192">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d02b1-192">ALIASES</span></span>

<span data-ttu-id="d02b1-193">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d02b1-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d02b1-194">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d02b1-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d02b1-195">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d02b1-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d02b1-196">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d02b1-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d02b1-197">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d02b1-198">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d02b1-199">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d02b1-200">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="d02b1-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d02b1-201">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d02b1-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d02b1-202">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="d02b1-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d02b1-203">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d02b1-204">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d02b1-205">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d02b1-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d02b1-206">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d02b1-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d02b1-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: a nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="d02b1-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="d02b1-208">`[Name <LanguageExtensionName?>]`: A nyelvi kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="d02b1-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="d02b1-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: a klaszter külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="d02b1-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="d02b1-210">`[Value <String>]`: A külső bérlőt képviselő GUID azonosító.</span><span class="sxs-lookup"><span data-stu-id="d02b1-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="d02b1-211">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d02b1-211">RELATED LINKS</span></span>

