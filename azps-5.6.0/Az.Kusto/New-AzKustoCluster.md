---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: c8378e9be3c92cc799eb92b9ff913be98116b019
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922410"
---
# <span data-ttu-id="d9abb-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d9abb-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="d9abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9abb-102">SYNOPSIS</span></span>
<span data-ttu-id="d9abb-103">Kusto-fürt létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="d9abb-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="d9abb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9abb-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9abb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9abb-105">DESCRIPTION</span></span>
<span data-ttu-id="d9abb-106">Kusto-fürt létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="d9abb-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="d9abb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9abb-107">EXAMPLES</span></span>

### <span data-ttu-id="d9abb-108">1. példa: Új Kusto-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="d9abb-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d9abb-109">A fenti parancs létrehoz egy "testnewkustocluster" nevű új Kusto-fürtöt a "testrg" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d9abb-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="d9abb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9abb-110">PARAMETERS</span></span>

### <span data-ttu-id="d9abb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9abb-111">-AsJob</span></span>
<span data-ttu-id="d9abb-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d9abb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d9abb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9abb-113">-DefaultProfile</span></span>
<span data-ttu-id="d9abb-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9abb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9abb-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d9abb-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="d9abb-116">Logikai érték, amely azt jelzi, hogy a fürt lemezei titkosítottak-e.</span><span class="sxs-lookup"><span data-stu-id="d9abb-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="d9abb-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="d9abb-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="d9abb-118">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a dupla titkosítás.</span><span class="sxs-lookup"><span data-stu-id="d9abb-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="d9abb-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="d9abb-119">-EnablePurge</span></span>
<span data-ttu-id="d9abb-120">Logikai érték, amely azt jelzi, hogy a véglegesen megadott műveletek engedélyezve vannak-e.</span><span class="sxs-lookup"><span data-stu-id="d9abb-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="d9abb-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="d9abb-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="d9abb-122">Logikai érték, amely azt jelzi, hogy engedélyezve van-e a folyamatos átvitel.</span><span class="sxs-lookup"><span data-stu-id="d9abb-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="d9abb-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="d9abb-123">-EngineType</span></span>
<span data-ttu-id="d9abb-124">A motor típusa</span><span class="sxs-lookup"><span data-stu-id="d9abb-124">The engine type</span></span>

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

### <span data-ttu-id="d9abb-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d9abb-125">-IdentityType</span></span>
<span data-ttu-id="d9abb-126">A használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="d9abb-126">The type of managed identity used.</span></span>
<span data-ttu-id="d9abb-127">A "SystemAssigned, UserAssigned" típus implicit módon létrehozott identitást és felhasználó által hozzárendelt identitásokat is tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d9abb-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="d9abb-128">A "Nincs" típus az összes identitást eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d9abb-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="d9abb-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d9abb-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="d9abb-130">A Kusto-fürthöz társított felhasználói identitások listája.</span><span class="sxs-lookup"><span data-stu-id="d9abb-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="d9abb-131">A felhasználói identitásszótár kulcshivatkozásai ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="d9abb-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="d9abb-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="d9abb-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="d9abb-133">A kulcs tárolókulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="d9abb-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="d9abb-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d9abb-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="d9abb-135">A kulcstár Uri-ja.</span><span class="sxs-lookup"><span data-stu-id="d9abb-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="d9abb-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d9abb-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="d9abb-137">A kulcs tárolókulcsának verziója.</span><span class="sxs-lookup"><span data-stu-id="d9abb-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="d9abb-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="d9abb-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="d9abb-139">A felhasználó által hozzárendelt identitás (ARM erőforrás-azonosító), amely hozzáféréssel rendelkezik a kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="d9abb-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="d9abb-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="d9abb-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="d9abb-141">A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="d9abb-141">The list of language extensions.</span></span>
<span data-ttu-id="d9abb-142">A felépítéshez a LANGUAGEEXTENSIONVALUE tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="d9abb-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d9abb-143">-Location</span><span class="sxs-lookup"><span data-stu-id="d9abb-143">-Location</span></span>
<span data-ttu-id="d9abb-144">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="d9abb-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="d9abb-145">-Name</span><span class="sxs-lookup"><span data-stu-id="d9abb-145">-Name</span></span>
<span data-ttu-id="d9abb-146">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d9abb-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9abb-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d9abb-147">-NoWait</span></span>
<span data-ttu-id="d9abb-148">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d9abb-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d9abb-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d9abb-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="d9abb-150">Logikai érték, amely azt jelzi, hogy az optimalizált automatikusskála funkció engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="d9abb-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="d9abb-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="d9abb-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="d9abb-152">A maximálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="d9abb-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="d9abb-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="d9abb-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="d9abb-154">A minimálisan engedélyezett példányok száma.</span><span class="sxs-lookup"><span data-stu-id="d9abb-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="d9abb-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="d9abb-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="d9abb-156">A sablon definiált verziója, például 1.</span><span class="sxs-lookup"><span data-stu-id="d9abb-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="d9abb-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9abb-157">-ResourceGroupName</span></span>
<span data-ttu-id="d9abb-158">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d9abb-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d9abb-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d9abb-159">-SkuCapacity</span></span>
<span data-ttu-id="d9abb-160">A fürt példányainak száma.</span><span class="sxs-lookup"><span data-stu-id="d9abb-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="d9abb-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d9abb-161">-SkuName</span></span>
<span data-ttu-id="d9abb-162">Termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="d9abb-162">SKU name.</span></span>

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

### <span data-ttu-id="d9abb-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d9abb-163">-SkuTier</span></span>
<span data-ttu-id="d9abb-164">Termékváltozatréteg.</span><span class="sxs-lookup"><span data-stu-id="d9abb-164">SKU tier.</span></span>

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

### <span data-ttu-id="d9abb-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9abb-165">-SubscriptionId</span></span>
<span data-ttu-id="d9abb-166">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d9abb-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9abb-167">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d9abb-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9abb-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9abb-168">-Tag</span></span>
<span data-ttu-id="d9abb-169">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="d9abb-169">Resource tags.</span></span>

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

### <span data-ttu-id="d9abb-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="d9abb-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="d9abb-171">A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="d9abb-171">The cluster's external tenants.</span></span>
<span data-ttu-id="d9abb-172">Ennek létrehozásáról a TRUSTEDEXTERNALTENANT tulajdonságokAT és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="d9abb-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d9abb-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="d9abb-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="d9abb-174">Adatkezelési nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9abb-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="d9abb-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="d9abb-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="d9abb-176">A motorszolgáltatás nyilvános IP-cím erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9abb-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="d9abb-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="d9abb-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="d9abb-178">Az alhálózati erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9abb-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="d9abb-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="d9abb-179">-Zone</span></span>
<span data-ttu-id="d9abb-180">A fürt elérhetőségi zónái.</span><span class="sxs-lookup"><span data-stu-id="d9abb-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="d9abb-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9abb-181">-Confirm</span></span>
<span data-ttu-id="d9abb-182">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d9abb-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9abb-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9abb-183">-WhatIf</span></span>
<span data-ttu-id="d9abb-184">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d9abb-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9abb-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9abb-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9abb-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9abb-186">CommonParameters</span></span>
<span data-ttu-id="d9abb-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9abb-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9abb-188">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9abb-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9abb-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9abb-189">INPUTS</span></span>

## <span data-ttu-id="d9abb-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9abb-190">OUTPUTS</span></span>

### <span data-ttu-id="d9abb-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="d9abb-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="d9abb-192">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9abb-192">NOTES</span></span>

<span data-ttu-id="d9abb-193">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d9abb-193">ALIASES</span></span>

<span data-ttu-id="d9abb-194">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d9abb-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9abb-195">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d9abb-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9abb-196">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9abb-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9abb-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: A nyelvi bővítmények listája.</span><span class="sxs-lookup"><span data-stu-id="d9abb-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="d9abb-198">`[Name <LanguageExtensionName?>]`: A nyelvbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="d9abb-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="d9abb-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: A fürt külső bérlői.</span><span class="sxs-lookup"><span data-stu-id="d9abb-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="d9abb-200">`[Value <String>]`: Külső bérlő guid azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9abb-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="d9abb-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9abb-201">RELATED LINKS</span></span>

