---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017776"
---
# <span data-ttu-id="e8fb8-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e8fb8-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="e8fb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8fb8-103">Frissíti a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e8fb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8fb8-104">SYNTAX</span></span>

### <span data-ttu-id="e8fb8-105">NamespaceParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8fb8-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8fb8-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8fb8-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8fb8-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8fb8-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8fb8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8fb8-108">DESCRIPTION</span></span>
<span data-ttu-id="e8fb8-109">A Set-AzEventHubNamespace parancsmag frissíti a megadott esemény-hubok névtér tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e8fb8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e8fb8-110">EXAMPLES</span></span>

### <span data-ttu-id="e8fb8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8fb8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="e8fb8-112">Frissíti a \` létrehozott névtér-MyNamespaceName címkéit \` .</span><span class="sxs-lookup"><span data-stu-id="e8fb8-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="e8fb8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e8fb8-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="e8fb8-114">A \` \` AutoInflate = enabled és a MaximumThroughputUnits = 10 névtér MyNamespaceName állapotát frissíti</span><span class="sxs-lookup"><span data-stu-id="e8fb8-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="e8fb8-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e8fb8-115">Example 3</span></span>

<span data-ttu-id="e8fb8-116">Frissíti a megadott esemény-hubok névteret.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="e8fb8-117">autogenerated</span><span class="sxs-lookup"><span data-stu-id="e8fb8-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="e8fb8-118">Példa 5: névtér létrehozása és frissítése a fürtökben lévő identitás kezelésével</span><span class="sxs-lookup"><span data-stu-id="e8fb8-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
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
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="e8fb8-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8fb8-119">PARAMETERS</span></span>

### <span data-ttu-id="e8fb8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8fb8-120">-DefaultProfile</span></span>
<span data-ttu-id="e8fb8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8fb8-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="e8fb8-122">-EnableAutoInflate</span></span>
<span data-ttu-id="e8fb8-123">Azt jelzi, hogy engedélyezve van-e a AutoInflate</span><span class="sxs-lookup"><span data-stu-id="e8fb8-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fb8-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="e8fb8-124">-EnableKafka</span></span>
<span data-ttu-id="e8fb8-125">a Kafka engedélyezése vagy letiltása a névtérhez</span><span class="sxs-lookup"><span data-stu-id="e8fb8-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="e8fb8-126">– Identitás</span><span class="sxs-lookup"><span data-stu-id="e8fb8-126">-Identity</span></span>
<span data-ttu-id="e8fb8-127">a névtér identitásának engedélyezése vagy letiltása</span><span class="sxs-lookup"><span data-stu-id="e8fb8-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="e8fb8-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="e8fb8-128">-IdentityUserDefined</span></span>
<span data-ttu-id="e8fb8-129">Felhasználó által definiált identitás vagy nincs</span><span class="sxs-lookup"><span data-stu-id="e8fb8-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fb8-130">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="e8fb8-130">-KeyProperty</span></span>
<span data-ttu-id="e8fb8-131">A főbb tulajdonságok listája, @ (@ (kulcsnév, KeyVaultUri, kulcskezelő), @ (kulcsnév, KeyVaultUri, saját verzió))</span><span class="sxs-lookup"><span data-stu-id="e8fb8-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fb8-132">-Forráskód</span><span class="sxs-lookup"><span data-stu-id="e8fb8-132">-KeySource</span></span>
<span data-ttu-id="e8fb8-133">Fő forrás</span><span class="sxs-lookup"><span data-stu-id="e8fb8-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fb8-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="e8fb8-134">-Location</span></span>
<span data-ttu-id="e8fb8-135">EventHub-névtér helye</span><span class="sxs-lookup"><span data-stu-id="e8fb8-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="e8fb8-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="e8fb8-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="e8fb8-137">Az átviteli egység felső korlátja, ha a AutoInflate engedélyezve van, az értéknek 0 – 20 átviteli egységen belül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fb8-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8fb8-138">-Name</span></span>
<span data-ttu-id="e8fb8-139">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="e8fb8-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="e8fb8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8fb8-140">-ResourceGroupName</span></span>
<span data-ttu-id="e8fb8-141">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="e8fb8-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e8fb8-142">-SkuCapacity</span></span>
<span data-ttu-id="e8fb8-143">A eventhub átviteli egységei.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="e8fb8-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e8fb8-144">-SkuName</span></span>
<span data-ttu-id="e8fb8-145">Namespace SKU Name (névtér)</span><span class="sxs-lookup"><span data-stu-id="e8fb8-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="e8fb8-146">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="e8fb8-146">-State</span></span>
<span data-ttu-id="e8fb8-147">A névtér letiltása/engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fb8-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="e8fb8-148">-Tag</span></span>
<span data-ttu-id="e8fb8-149">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fb8-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8fb8-150">-Confirm</span></span>
<span data-ttu-id="e8fb8-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8fb8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8fb8-152">-WhatIf</span></span>
<span data-ttu-id="e8fb8-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8fb8-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8fb8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8fb8-155">CommonParameters</span></span>
<span data-ttu-id="e8fb8-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8fb8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8fb8-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8fb8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8fb8-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8fb8-158">INPUTS</span></span>

### <span data-ttu-id="e8fb8-159">System. String</span><span class="sxs-lookup"><span data-stu-id="e8fb8-159">System.String</span></span>

### <span data-ttu-id="e8fb8-160">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e8fb8-161">System. null ' 1 [[Microsoft. Azure. commands. EventHub. models. NamespaceState, Microsoft. Azure. PowerShell. parancsmagok. EventHub, Version = 1.4.3.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e8fb8-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e8fb8-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8fb8-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e8fb8-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8fb8-163">OUTPUTS</span></span>

### <span data-ttu-id="e8fb8-164">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e8fb8-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e8fb8-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8fb8-165">NOTES</span></span>

## <span data-ttu-id="e8fb8-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8fb8-166">RELATED LINKS</span></span>
