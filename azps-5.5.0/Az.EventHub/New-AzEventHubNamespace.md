---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155682"
---
# <span data-ttu-id="7e78e-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7e78e-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="7e78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e78e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e78e-103">Létrehozza az Eseményközpontok névterét.</span><span class="sxs-lookup"><span data-stu-id="7e78e-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="7e78e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e78e-104">SYNTAX</span></span>

### <span data-ttu-id="7e78e-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e78e-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e78e-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e78e-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e78e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e78e-107">DESCRIPTION</span></span>
<span data-ttu-id="7e78e-108">A New-AzEventHubNamespace parancsmag létrehoz egy új névteret az Eseményközpontok típushoz.</span><span class="sxs-lookup"><span data-stu-id="7e78e-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="7e78e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e78e-109">EXAMPLES</span></span>
### <span data-ttu-id="7e78e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e78e-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7e78e-111">Létrehoz egy Event Hubs névteret MyNamespaceName a MyLocation megadott földrajzi \` \` \` \` helyén, a \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7e78e-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7e78e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7e78e-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7e78e-113">Létrehoz egy Event Hubs namespace MyNamespaceName értéket a MyLocation megadott földrajzi helyen, a MyResourceGroupName és az AutoInflate erőforráscsoportban engedélyezve van a \` \` \` \` \` \` MaximumThroughputUnits 10 esetén.</span><span class="sxs-lookup"><span data-stu-id="7e78e-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="7e78e-114">3. példa: Kafka-kompatibilis névtér</span><span class="sxs-lookup"><span data-stu-id="7e78e-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7e78e-115">Létrehoz egy Event Hubs névteret MyNamespaceName a myLocation megadott földrajzi helyen, a \` \` \` \` \` MyResourceGroupName erőforráscsoportban, ahol a Kafka és az \` Automatikusinflate beállítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="7e78e-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="7e78e-116">4. példa: ZoneRedundant enabled namespace</span><span class="sxs-lookup"><span data-stu-id="7e78e-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7e78e-117">Létrehoz egy Event Hubs névteret MyNamespaceName a myLocation megadott földrajzi helyen, a \` \` \` \` \` MyResourceGroupName erőforráscsoportban, ahol a Kafka és az \` Automatikusinflate beállítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="7e78e-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="7e78e-118">5. példa: Névtér létrehozása az identitás kezelése fürtben</span><span class="sxs-lookup"><span data-stu-id="7e78e-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :


# Get created namespace
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="7e78e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e78e-119">PARAMETERS</span></span>

### <span data-ttu-id="7e78e-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="7e78e-120">-ClusterARMId</span></span>
<span data-ttu-id="7e78e-121">ARM a fürt azonosítója, ahol a névteret létre kell hozva</span><span class="sxs-lookup"><span data-stu-id="7e78e-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e78e-122">-DefaultProfile</span></span>
<span data-ttu-id="7e78e-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e78e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e78e-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="7e78e-124">-EnableAutoInflate</span></span>
<span data-ttu-id="7e78e-125">Azt jelzi, hogy engedélyezve van-e az Automatikusinflate funkció</span><span class="sxs-lookup"><span data-stu-id="7e78e-125">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="7e78e-126">-EnableKafka</span></span>
<span data-ttu-id="7e78e-127">A Kafka névtérhez való engedélyezése vagy letiltása</span><span class="sxs-lookup"><span data-stu-id="7e78e-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="7e78e-128">-Identity</span><span class="sxs-lookup"><span data-stu-id="7e78e-128">-Identity</span></span>
<span data-ttu-id="7e78e-129">Az Identity for namespace engedélyezése vagy letiltása</span><span class="sxs-lookup"><span data-stu-id="7e78e-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="7e78e-130">-Location</span><span class="sxs-lookup"><span data-stu-id="7e78e-130">-Location</span></span>
<span data-ttu-id="7e78e-131">EventHub Namespace Location.</span><span class="sxs-lookup"><span data-stu-id="7e78e-131">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="7e78e-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="7e78e-133">Az automatikus átflate beállítás engedélyezése esetén az átviteli sebesség felső határa, az értéknek 0 és 20 átviteli egység között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7e78e-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7e78e-134">-Name</span></span>
<span data-ttu-id="7e78e-135">EventHub Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="7e78e-135">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e78e-136">-ResourceGroupName</span></span>
<span data-ttu-id="7e78e-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7e78e-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7e78e-138">-SkuCapacity</span></span>
<span data-ttu-id="7e78e-139">Az eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="7e78e-139">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7e78e-140">-SkuName</span></span>
<span data-ttu-id="7e78e-141">Névtér-termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="7e78e-141">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e78e-142">-Tag</span></span>
<span data-ttu-id="7e78e-143">Az erőforráscímkéket képviselő hashtables.</span><span class="sxs-lookup"><span data-stu-id="7e78e-143">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e78e-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7e78e-144">-ZoneRedundant</span></span>
<span data-ttu-id="7e78e-145">A névtér redundáns zóna engedélyezése vagy letiltása</span><span class="sxs-lookup"><span data-stu-id="7e78e-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="7e78e-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e78e-146">-Confirm</span></span>
<span data-ttu-id="7e78e-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e78e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e78e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e78e-148">-WhatIf</span></span>
<span data-ttu-id="7e78e-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e78e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e78e-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e78e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e78e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e78e-151">CommonParameters</span></span>
<span data-ttu-id="7e78e-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e78e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e78e-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e78e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e78e-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e78e-154">INPUTS</span></span>

### <span data-ttu-id="7e78e-155">System.String</span><span class="sxs-lookup"><span data-stu-id="7e78e-155">System.String</span></span>

### <span data-ttu-id="7e78e-156">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7e78e-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7e78e-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e78e-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e78e-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e78e-158">OUTPUTS</span></span>

### <span data-ttu-id="7e78e-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7e78e-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7e78e-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e78e-160">NOTES</span></span>

## <span data-ttu-id="7e78e-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e78e-161">RELATED LINKS</span></span>
