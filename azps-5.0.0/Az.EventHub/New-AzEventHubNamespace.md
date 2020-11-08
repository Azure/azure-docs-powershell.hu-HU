---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185464"
---
# <span data-ttu-id="df7a0-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="df7a0-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="df7a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="df7a0-103">Esemény-hubok névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="df7a0-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="df7a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df7a0-104">SYNTAX</span></span>

### <span data-ttu-id="df7a0-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df7a0-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df7a0-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="df7a0-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df7a0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df7a0-107">DESCRIPTION</span></span>
<span data-ttu-id="df7a0-108">A New-AzEventHubNamespace parancsmag az esemény típusú hubok új névterét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="df7a0-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="df7a0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df7a0-109">EXAMPLES</span></span>
### <span data-ttu-id="df7a0-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="df7a0-110">Example 1</span></span>                                           
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

<span data-ttu-id="df7a0-111">A \` \` megadott földrajzi hely \` MyLocation \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény-hubok névtér-MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="df7a0-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="df7a0-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="df7a0-112">Example 2</span></span>
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

<span data-ttu-id="df7a0-113">Létrehozza az esemény-hubok \` névtér \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName \` és a AutoInflate engedélyezve van a MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="df7a0-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="df7a0-114">3. példa: Kafka engedélyezve névtér</span><span class="sxs-lookup"><span data-stu-id="df7a0-114">Example 3: Kafka enabled namespace</span></span>
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

<span data-ttu-id="df7a0-115">Az esemény-hubok névtér \` \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName a \` Kafka-és AutoInflate engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="df7a0-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="df7a0-116">4. példa: ZoneRedundant engedélyezve névtér</span><span class="sxs-lookup"><span data-stu-id="df7a0-116">Example 4: ZoneRedundant enabled namespace</span></span>
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

<span data-ttu-id="df7a0-117">Az esemény-hubok névtér \` \` -MyNamespaceName a megadott földrajzi hely \` MyLocation \` , az erőforráscsoport \` MyResourceGroupName a \` Kafka-és AutoInflate engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="df7a0-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="df7a0-118">Példa 5: névtér létrehozása fürtben lévő identitás kezelésével</span><span class="sxs-lookup"><span data-stu-id="df7a0-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="df7a0-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df7a0-119">PARAMETERS</span></span>

### <span data-ttu-id="df7a0-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="df7a0-120">-ClusterARMId</span></span>
<span data-ttu-id="df7a0-121">A névteret létrehozó fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="df7a0-121">ARM ID of Cluster where namespace is to be created</span></span>

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

### <span data-ttu-id="df7a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7a0-122">-DefaultProfile</span></span>
<span data-ttu-id="df7a0-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df7a0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df7a0-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="df7a0-124">-EnableAutoInflate</span></span>
<span data-ttu-id="df7a0-125">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="df7a0-125">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="df7a0-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="df7a0-126">-EnableKafka</span></span>
<span data-ttu-id="df7a0-127">a Kafka engedélyezése vagy letiltása a névtérhez</span><span class="sxs-lookup"><span data-stu-id="df7a0-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="df7a0-128">– Identitás</span><span class="sxs-lookup"><span data-stu-id="df7a0-128">-Identity</span></span>
<span data-ttu-id="df7a0-129">a névtér identitásának engedélyezése vagy letiltása</span><span class="sxs-lookup"><span data-stu-id="df7a0-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="df7a0-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="df7a0-130">-Location</span></span>
<span data-ttu-id="df7a0-131">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="df7a0-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="df7a0-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="df7a0-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="df7a0-133">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="df7a0-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="df7a0-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df7a0-134">-Name</span></span>
<span data-ttu-id="df7a0-135">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="df7a0-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="df7a0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7a0-136">-ResourceGroupName</span></span>
<span data-ttu-id="df7a0-137">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="df7a0-137">Resource Group Name</span></span>

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

### <span data-ttu-id="df7a0-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="df7a0-138">-SkuCapacity</span></span>
<span data-ttu-id="df7a0-139">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="df7a0-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="df7a0-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="df7a0-140">-SkuName</span></span>
<span data-ttu-id="df7a0-141">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="df7a0-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="df7a0-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="df7a0-142">-Tag</span></span>
<span data-ttu-id="df7a0-143">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="df7a0-143">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="df7a0-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="df7a0-144">-ZoneRedundant</span></span>
<span data-ttu-id="df7a0-145">a redundáns zónák engedélyezése vagy letiltása a névtérhez</span><span class="sxs-lookup"><span data-stu-id="df7a0-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="df7a0-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df7a0-146">-Confirm</span></span>
<span data-ttu-id="df7a0-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df7a0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7a0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7a0-148">-WhatIf</span></span>
<span data-ttu-id="df7a0-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df7a0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7a0-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df7a0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7a0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7a0-151">CommonParameters</span></span>
<span data-ttu-id="df7a0-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df7a0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7a0-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="df7a0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7a0-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df7a0-154">INPUTS</span></span>

### <span data-ttu-id="df7a0-155">System. String</span><span class="sxs-lookup"><span data-stu-id="df7a0-155">System.String</span></span>

### <span data-ttu-id="df7a0-156">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="df7a0-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="df7a0-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="df7a0-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="df7a0-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df7a0-158">OUTPUTS</span></span>

### <span data-ttu-id="df7a0-159">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="df7a0-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="df7a0-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df7a0-160">NOTES</span></span>

## <span data-ttu-id="df7a0-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df7a0-161">RELATED LINKS</span></span>
