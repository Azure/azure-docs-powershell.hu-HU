---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366896"
---
# <span data-ttu-id="044a5-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="044a5-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="044a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="044a5-102">SYNOPSIS</span></span>
<span data-ttu-id="044a5-103">Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="044a5-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="044a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="044a5-104">SYNTAX</span></span>

### <span data-ttu-id="044a5-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="044a5-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="044a5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="044a5-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="044a5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="044a5-107">DESCRIPTION</span></span>
<span data-ttu-id="044a5-108">Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="044a5-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="044a5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="044a5-109">EXAMPLES</span></span>

### <span data-ttu-id="044a5-110">1. példa: Meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="044a5-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="044a5-111">A fenti parancs frissíti a Kusto-fürt "testnewkustocluster" termékváltozatát, amely a "testrg" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="044a5-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="044a5-112">2. példa: Meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="044a5-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="044a5-113">A fenti parancs egy ügyfél által kezelt kulccsal frissíti a "testrg" erőforráscsoportban található "testnewkustocluster" fürtöt.</span><span class="sxs-lookup"><span data-stu-id="044a5-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="044a5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="044a5-114">PARAMETERS</span></span>

### <span data-ttu-id="044a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="044a5-115">-AsJob</span></span>
<span data-ttu-id="044a5-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="044a5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="044a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044a5-117">-DefaultProfile</span></span>
<span data-ttu-id="044a5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="044a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="044a5-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="044a5-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="044a5-120">Logikai érték, amely azt jelzi, hogy a fürt lemezei titkosítottak-e.</span><span class="sxs-lookup"><span data-stu-id="044a5-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="044a5-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="044a5-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="044a5-122">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a dupla titkosítás.</span><span class="sxs-lookup"><span data-stu-id="044a5-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="044a5-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="044a5-123">-EnablePurge</span></span>
<span data-ttu-id="044a5-124">Logikai érték, amely azt jelzi, hogy a véglegesen megadott műveletek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="044a5-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="044a5-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="044a5-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="044a5-126">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a folyamatos átvitel.</span><span class="sxs-lookup"><span data-stu-id="044a5-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="044a5-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="044a5-127">-IdentityType</span></span>
<span data-ttu-id="044a5-128">Az identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="044a5-128">The identity type.</span></span>

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

### <span data-ttu-id="044a5-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="044a5-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="044a5-130">A Kusto-fürthöz társított felhasználói identitások listája.</span><span class="sxs-lookup"><span data-stu-id="044a5-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="044a5-131">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="044a5-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="044a5-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="044a5-132">-InputObject</span></span>
<span data-ttu-id="044a5-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="044a5-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="044a5-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="044a5-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="044a5-135">A kulcs tárolókulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="044a5-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="044a5-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="044a5-137">A kulcstár Uri-ja.</span><span class="sxs-lookup"><span data-stu-id="044a5-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="044a5-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="044a5-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="044a5-139">A kulcs tárolókulcsának verziója.</span><span class="sxs-lookup"><span data-stu-id="044a5-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="044a5-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="044a5-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="044a5-141">A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="044a5-141">The list of language extensions.</span></span>
<span data-ttu-id="044a5-142">A felépítéshez a LANGUAGEEXTENSIONVALUE tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="044a5-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="044a5-143">-Location</span><span class="sxs-lookup"><span data-stu-id="044a5-143">-Location</span></span>
<span data-ttu-id="044a5-144">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="044a5-144">Resource location.</span></span>

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

### <span data-ttu-id="044a5-145">-Name</span><span class="sxs-lookup"><span data-stu-id="044a5-145">-Name</span></span>
<span data-ttu-id="044a5-146">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="044a5-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="044a5-147">-NoWait</span></span>
<span data-ttu-id="044a5-148">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="044a5-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="044a5-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="044a5-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="044a5-150">Logikai érték, amely azt jelzi, hogy az optimalizált automatikusskála funkció engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="044a5-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="044a5-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="044a5-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="044a5-152">A maximálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="044a5-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="044a5-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="044a5-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="044a5-154">A minimálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="044a5-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="044a5-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="044a5-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="044a5-156">A sablon definiált verziója, például 1.</span><span class="sxs-lookup"><span data-stu-id="044a5-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="044a5-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044a5-157">-ResourceGroupName</span></span>
<span data-ttu-id="044a5-158">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="044a5-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="044a5-159">-SkuCapacity</span></span>
<span data-ttu-id="044a5-160">A fürt példányainak száma.</span><span class="sxs-lookup"><span data-stu-id="044a5-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="044a5-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="044a5-161">-SkuName</span></span>
<span data-ttu-id="044a5-162">Termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-162">SKU name.</span></span>

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

### <span data-ttu-id="044a5-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="044a5-163">-SkuTier</span></span>
<span data-ttu-id="044a5-164">Termékváltozatréteg.</span><span class="sxs-lookup"><span data-stu-id="044a5-164">SKU tier.</span></span>

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

### <span data-ttu-id="044a5-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="044a5-165">-SubscriptionId</span></span>
<span data-ttu-id="044a5-166">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="044a5-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="044a5-167">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="044a5-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="044a5-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="044a5-168">-Tag</span></span>
<span data-ttu-id="044a5-169">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="044a5-169">Resource tags.</span></span>

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

### <span data-ttu-id="044a5-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="044a5-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="044a5-171">A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="044a5-171">The cluster's external tenants.</span></span>
<span data-ttu-id="044a5-172">Ennek létrehozásáról a TRUSTEDEXTERNALTENANT tulajdonságokAT és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="044a5-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="044a5-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="044a5-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="044a5-174">Adatkezelési nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="044a5-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="044a5-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="044a5-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="044a5-176">A motorszolgáltatás nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="044a5-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="044a5-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="044a5-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="044a5-178">Az alhálózati erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="044a5-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="044a5-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="044a5-179">-Confirm</span></span>
<span data-ttu-id="044a5-180">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="044a5-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044a5-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044a5-181">-WhatIf</span></span>
<span data-ttu-id="044a5-182">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="044a5-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044a5-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="044a5-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044a5-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044a5-184">CommonParameters</span></span>
<span data-ttu-id="044a5-185">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="044a5-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044a5-186">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="044a5-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044a5-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="044a5-187">INPUTS</span></span>

### <span data-ttu-id="044a5-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="044a5-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="044a5-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="044a5-189">OUTPUTS</span></span>

### <span data-ttu-id="044a5-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span><span class="sxs-lookup"><span data-stu-id="044a5-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="044a5-191">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="044a5-191">NOTES</span></span>

<span data-ttu-id="044a5-192">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="044a5-192">ALIASES</span></span>

<span data-ttu-id="044a5-193">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="044a5-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="044a5-194">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="044a5-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="044a5-195">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="044a5-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="044a5-196">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="044a5-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="044a5-197">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="044a5-198">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="044a5-199">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="044a5-200">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="044a5-201">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="044a5-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="044a5-202">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="044a5-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="044a5-203">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="044a5-204">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="044a5-205">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="044a5-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="044a5-206">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="044a5-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="044a5-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="044a5-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="044a5-208">`[Name <LanguageExtensionName?>]`: A nyelvbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="044a5-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="044a5-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="044a5-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="044a5-210">`[Value <String>]`: Külső bérlő guid azonosítója.</span><span class="sxs-lookup"><span data-stu-id="044a5-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="044a5-211">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="044a5-211">RELATED LINKS</span></span>

