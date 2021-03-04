---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 21a2869a7a8006fdc0a570ebf4176f28c3a44efc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932809"
---
# <span data-ttu-id="9bd8e-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="9bd8e-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="9bd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd8e-103">Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="9bd8e-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="9bd8e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9bd8e-104">SYNTAX</span></span>

### <span data-ttu-id="9bd8e-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bd8e-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9bd8e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9bd8e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9bd8e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9bd8e-107">DESCRIPTION</span></span>
<span data-ttu-id="9bd8e-108">Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="9bd8e-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="9bd8e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9bd8e-109">EXAMPLES</span></span>

### <span data-ttu-id="9bd8e-110">1. példa: Meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="9bd8e-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="9bd8e-111">A fenti parancs frissíti a Kusto-fürt "testnewkustocluster" termékváltozatát, amely a "testrg" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="9bd8e-112">2. példa: Meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="9bd8e-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="9bd8e-113">A fenti parancs egy ügyfél által kezelt kulccsal frissíti a "testrg" erőforráscsoportban található "testnewkustocluster" fürtöt.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="9bd8e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bd8e-114">PARAMETERS</span></span>

### <span data-ttu-id="9bd8e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bd8e-115">-AsJob</span></span>
<span data-ttu-id="9bd8e-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="9bd8e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9bd8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd8e-117">-DefaultProfile</span></span>
<span data-ttu-id="9bd8e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd8e-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9bd8e-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="9bd8e-120">Logikai érték, amely azt jelzi, hogy a fürt lemezei titkosítottak-e.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="9bd8e-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="9bd8e-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="9bd8e-122">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a dupla titkosítás.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="9bd8e-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="9bd8e-123">-EnablePurge</span></span>
<span data-ttu-id="9bd8e-124">Logikai érték, amely azt jelzi, hogy a véglegesen megadott műveletek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="9bd8e-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="9bd8e-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="9bd8e-126">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a folyamatos átvitel.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="9bd8e-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="9bd8e-127">-EngineType</span></span>
<span data-ttu-id="9bd8e-128">A motor típusa</span><span class="sxs-lookup"><span data-stu-id="9bd8e-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd8e-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9bd8e-129">-IdentityType</span></span>
<span data-ttu-id="9bd8e-130">A használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-130">The type of managed identity used.</span></span>
<span data-ttu-id="9bd8e-131">A "SystemAssigned, UserAssigned" típus implicit módon létrehozott identitást és felhasználó által hozzárendelt identitásokat is tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="9bd8e-132">A "Nincs" típus az összes identitást eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="9bd8e-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9bd8e-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="9bd8e-134">A Kusto-fürthöz társított felhasználói identitások listája.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="9bd8e-135">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="9bd8e-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bd8e-136">-InputObject</span></span>
<span data-ttu-id="9bd8e-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9bd8e-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="9bd8e-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="9bd8e-139">A kulcs tárolókulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="9bd8e-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9bd8e-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="9bd8e-141">A kulcstár Uri-ja.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="9bd8e-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="9bd8e-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="9bd8e-143">A kulcs tárolókulcsának verziója.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="9bd8e-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="9bd8e-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="9bd8e-145">A felhasználó által hozzárendelt identitás (ARM erőforrás-azonosító), amely hozzáféréssel rendelkezik a kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="9bd8e-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="9bd8e-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="9bd8e-147">A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-147">The list of language extensions.</span></span>
<span data-ttu-id="9bd8e-148">A felépítéshez a LANGUAGEEXTENSIONVALUE tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd8e-149">-Location</span><span class="sxs-lookup"><span data-stu-id="9bd8e-149">-Location</span></span>
<span data-ttu-id="9bd8e-150">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-150">Resource location.</span></span>

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

### <span data-ttu-id="9bd8e-151">-Name</span><span class="sxs-lookup"><span data-stu-id="9bd8e-151">-Name</span></span>
<span data-ttu-id="9bd8e-152">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-152">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9bd8e-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9bd8e-153">-NoWait</span></span>
<span data-ttu-id="9bd8e-154">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="9bd8e-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9bd8e-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="9bd8e-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="9bd8e-156">Logikai érték, amely azt jelzi, hogy az optimalizált automatikusskála funkció engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="9bd8e-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="9bd8e-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="9bd8e-158">A maximálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="9bd8e-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="9bd8e-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="9bd8e-160">A minimálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="9bd8e-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="9bd8e-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="9bd8e-162">A sablon definiált verziója, például 1.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="9bd8e-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd8e-163">-ResourceGroupName</span></span>
<span data-ttu-id="9bd8e-164">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9bd8e-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9bd8e-165">-SkuCapacity</span></span>
<span data-ttu-id="9bd8e-166">A fürt példányainak száma.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="9bd8e-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9bd8e-167">-SkuName</span></span>
<span data-ttu-id="9bd8e-168">Termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-168">SKU name.</span></span>

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

### <span data-ttu-id="9bd8e-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9bd8e-169">-SkuTier</span></span>
<span data-ttu-id="9bd8e-170">Termékváltozatréteg.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-170">SKU tier.</span></span>

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

### <span data-ttu-id="9bd8e-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bd8e-171">-SubscriptionId</span></span>
<span data-ttu-id="9bd8e-172">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9bd8e-173">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9bd8e-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="9bd8e-174">-Tag</span></span>
<span data-ttu-id="9bd8e-175">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-175">Resource tags.</span></span>

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

### <span data-ttu-id="9bd8e-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="9bd8e-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="9bd8e-177">A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-177">The cluster's external tenants.</span></span>
<span data-ttu-id="9bd8e-178">Ennek létrehozásáról a TRUSTEDEXTERNALTENANT tulajdonságokAT és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd8e-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="9bd8e-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="9bd8e-180">Adatkezelési nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="9bd8e-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="9bd8e-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="9bd8e-182">A motorszolgáltatás nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="9bd8e-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="9bd8e-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="9bd8e-184">Az alhálózati erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="9bd8e-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bd8e-185">-Confirm</span></span>
<span data-ttu-id="9bd8e-186">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd8e-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd8e-187">-WhatIf</span></span>
<span data-ttu-id="9bd8e-188">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd8e-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd8e-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd8e-190">CommonParameters</span></span>
<span data-ttu-id="9bd8e-191">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd8e-192">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bd8e-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd8e-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bd8e-193">INPUTS</span></span>

### <span data-ttu-id="9bd8e-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9bd8e-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9bd8e-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bd8e-195">OUTPUTS</span></span>

### <span data-ttu-id="9bd8e-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="9bd8e-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="9bd8e-197">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9bd8e-197">NOTES</span></span>

<span data-ttu-id="9bd8e-198">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9bd8e-198">ALIASES</span></span>

<span data-ttu-id="9bd8e-199">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9bd8e-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9bd8e-200">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9bd8e-201">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9bd8e-202">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9bd8e-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9bd8e-203">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9bd8e-204">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9bd8e-205">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9bd8e-206">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9bd8e-207">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9bd8e-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9bd8e-208">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9bd8e-209">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9bd8e-210">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9bd8e-211">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9bd8e-212">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="9bd8e-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="9bd8e-214">`[Name <LanguageExtensionName?>]`: A nyelvbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="9bd8e-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="9bd8e-216">`[Value <String>]`: Külső bérlő guid azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9bd8e-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="9bd8e-217">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bd8e-217">RELATED LINKS</span></span>

