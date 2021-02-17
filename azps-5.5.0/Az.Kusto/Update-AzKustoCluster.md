---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147651"
---
# <span data-ttu-id="d07f5-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d07f5-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="d07f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d07f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d07f5-103">Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="d07f5-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="d07f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d07f5-104">SYNTAX</span></span>

### <span data-ttu-id="d07f5-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d07f5-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="d07f5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d07f5-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="d07f5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d07f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d07f5-108">Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="d07f5-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="d07f5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d07f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d07f5-110">1. példa: Meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d07f5-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d07f5-111">A fenti parancs frissíti a Kusto-fürt "testnewkustocluster" termékváltozatát, amely a "testrg" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="d07f5-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d07f5-112">2. példa: Meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d07f5-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d07f5-113">A fenti parancs egy ügyfél által kezelt kulccsal frissíti a "testrg" erőforráscsoportban található "testnewkustocluster" fürtöt.</span><span class="sxs-lookup"><span data-stu-id="d07f5-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="d07f5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d07f5-114">PARAMETERS</span></span>

### <span data-ttu-id="d07f5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d07f5-115">-AsJob</span></span>
<span data-ttu-id="d07f5-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d07f5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d07f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07f5-117">-DefaultProfile</span></span>
<span data-ttu-id="d07f5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d07f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d07f5-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d07f5-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="d07f5-120">Logikai érték, amely azt jelzi, hogy a fürt lemezei titkosítottak-e.</span><span class="sxs-lookup"><span data-stu-id="d07f5-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="d07f5-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="d07f5-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="d07f5-122">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a dupla titkosítás.</span><span class="sxs-lookup"><span data-stu-id="d07f5-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="d07f5-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="d07f5-123">-EnablePurge</span></span>
<span data-ttu-id="d07f5-124">Logikai érték, amely azt jelzi, hogy a véglegesen megadott műveletek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="d07f5-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="d07f5-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="d07f5-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="d07f5-126">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a folyamatos átvitel.</span><span class="sxs-lookup"><span data-stu-id="d07f5-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="d07f5-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="d07f5-127">-EngineType</span></span>
<span data-ttu-id="d07f5-128">A motor típusa</span><span class="sxs-lookup"><span data-stu-id="d07f5-128">The engine type</span></span>

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

### <span data-ttu-id="d07f5-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d07f5-129">-IdentityType</span></span>
<span data-ttu-id="d07f5-130">A használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="d07f5-130">The type of managed identity used.</span></span>
<span data-ttu-id="d07f5-131">A "SystemAssigned, UserAssigned" típus implicit módon létrehozott identitást és felhasználó által hozzárendelt identitásokat is tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d07f5-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="d07f5-132">A "Nincs" típus az összes identitást eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d07f5-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="d07f5-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d07f5-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="d07f5-134">A Kusto-fürthöz társított felhasználói identitások listája.</span><span class="sxs-lookup"><span data-stu-id="d07f5-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="d07f5-135">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="d07f5-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="d07f5-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d07f5-136">-InputObject</span></span>
<span data-ttu-id="d07f5-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d07f5-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d07f5-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="d07f5-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="d07f5-139">A kulcs tárolókulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="d07f5-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d07f5-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="d07f5-141">A kulcstár Uri-ja.</span><span class="sxs-lookup"><span data-stu-id="d07f5-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="d07f5-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d07f5-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="d07f5-143">A kulcs tárolókulcsának verziója.</span><span class="sxs-lookup"><span data-stu-id="d07f5-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="d07f5-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="d07f5-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="d07f5-145">A felhasználó által hozzárendelt identitás (ARM erőforrás-azonosító), amely hozzáféréssel rendelkezik a kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="d07f5-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="d07f5-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="d07f5-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="d07f5-147">A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="d07f5-147">The list of language extensions.</span></span>
<span data-ttu-id="d07f5-148">A felépítésről a NOTES (MEGJEGYZÉSEK) szakaszban láthatja a LANGUAGEEXTENSIONVALUE tulajdonságokat, és létrehozhat egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="d07f5-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d07f5-149">-Location</span><span class="sxs-lookup"><span data-stu-id="d07f5-149">-Location</span></span>
<span data-ttu-id="d07f5-150">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d07f5-150">Resource location.</span></span>

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

### <span data-ttu-id="d07f5-151">-Name</span><span class="sxs-lookup"><span data-stu-id="d07f5-151">-Name</span></span>
<span data-ttu-id="d07f5-152">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-152">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d07f5-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d07f5-153">-NoWait</span></span>
<span data-ttu-id="d07f5-154">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d07f5-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d07f5-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d07f5-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="d07f5-156">Logikai érték, amely azt jelzi, hogy az optimalizált automatikusskála funkció engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="d07f5-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="d07f5-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="d07f5-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="d07f5-158">A maximálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="d07f5-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="d07f5-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="d07f5-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="d07f5-160">A minimálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="d07f5-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="d07f5-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="d07f5-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="d07f5-162">A sablon definiált verziója, például 1.</span><span class="sxs-lookup"><span data-stu-id="d07f5-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="d07f5-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07f5-163">-ResourceGroupName</span></span>
<span data-ttu-id="d07f5-164">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d07f5-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d07f5-165">-SkuCapacity</span></span>
<span data-ttu-id="d07f5-166">A fürt példányainak száma.</span><span class="sxs-lookup"><span data-stu-id="d07f5-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="d07f5-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d07f5-167">-SkuName</span></span>
<span data-ttu-id="d07f5-168">Termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-168">SKU name.</span></span>

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

### <span data-ttu-id="d07f5-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d07f5-169">-SkuTier</span></span>
<span data-ttu-id="d07f5-170">Termékváltozatréteg.</span><span class="sxs-lookup"><span data-stu-id="d07f5-170">SKU tier.</span></span>

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

### <span data-ttu-id="d07f5-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d07f5-171">-SubscriptionId</span></span>
<span data-ttu-id="d07f5-172">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d07f5-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d07f5-173">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d07f5-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d07f5-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="d07f5-174">-Tag</span></span>
<span data-ttu-id="d07f5-175">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="d07f5-175">Resource tags.</span></span>

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

### <span data-ttu-id="d07f5-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="d07f5-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="d07f5-177">A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="d07f5-177">The cluster's external tenants.</span></span>
<span data-ttu-id="d07f5-178">Ennek létrehozásáról a TRUSTEDEXTERNALTENANT tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="d07f5-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d07f5-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="d07f5-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="d07f5-180">Adatkezelési nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d07f5-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="d07f5-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="d07f5-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="d07f5-182">A motorszolgáltatás nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d07f5-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="d07f5-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="d07f5-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="d07f5-184">Az alhálózati erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d07f5-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="d07f5-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d07f5-185">-Confirm</span></span>
<span data-ttu-id="d07f5-186">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d07f5-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d07f5-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07f5-187">-WhatIf</span></span>
<span data-ttu-id="d07f5-188">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d07f5-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07f5-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d07f5-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d07f5-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07f5-190">CommonParameters</span></span>
<span data-ttu-id="d07f5-191">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d07f5-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07f5-192">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d07f5-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07f5-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d07f5-193">INPUTS</span></span>

### <span data-ttu-id="d07f5-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d07f5-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d07f5-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d07f5-195">OUTPUTS</span></span>

### <span data-ttu-id="d07f5-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="d07f5-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="d07f5-197">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d07f5-197">NOTES</span></span>

<span data-ttu-id="d07f5-198">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d07f5-198">ALIASES</span></span>

<span data-ttu-id="d07f5-199">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d07f5-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d07f5-200">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d07f5-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d07f5-201">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d07f5-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d07f5-202">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d07f5-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d07f5-203">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d07f5-204">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d07f5-205">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d07f5-206">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d07f5-207">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d07f5-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d07f5-208">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="d07f5-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d07f5-209">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment név.</span><span class="sxs-lookup"><span data-stu-id="d07f5-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d07f5-210">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d07f5-211">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d07f5-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d07f5-212">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d07f5-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d07f5-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="d07f5-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="d07f5-214">`[Name <LanguageExtensionName?>]`: A nyelvbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="d07f5-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="d07f5-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="d07f5-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="d07f5-216">`[Value <String>]`: Külső bérlő guid azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d07f5-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="d07f5-217">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d07f5-217">RELATED LINKS</span></span>

