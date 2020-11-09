---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301169"
---
# <span data-ttu-id="e1b29-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="e1b29-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="e1b29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1b29-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b29-103">Get-AzPolicyAlias beolvassa és kinyeri az Azure-szolgáltató erőforrás-típusait, amelyek a megadott paraméter-értékekkel rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="e1b29-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="e1b29-104">Ha nincs paraméter megadva, a rendszer minden olyan szolgáltatói erőforrástípust exportál, amely aliast tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e1b29-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="e1b29-105">A-ListAvailable kapcsoló a megfelelő erőforrástípusok (aliasok nélkül) megadásával módosítja ezt a problémát.</span><span class="sxs-lookup"><span data-stu-id="e1b29-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="e1b29-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1b29-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1b29-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1b29-107">DESCRIPTION</span></span>
<span data-ttu-id="e1b29-108">A **Get-AzPolicyAlias** parancsmag a házirend-aliasok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e1b29-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="e1b29-109">A házirend-aliasokat az Azure-házirend használja az erőforrás típusa tulajdonságra való hivatkozáshoz.</span><span class="sxs-lookup"><span data-stu-id="e1b29-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="e1b29-110">A paraméterek abban az módon jelennek meg, hogy a lista elemeinek korlátozása az erőforrás típusa vagy az aliasai különböző tulajdonságaival egyező módon történik.</span><span class="sxs-lookup"><span data-stu-id="e1b29-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="e1b29-111">A megadott egyezési érték megegyezik abban az esetben, ha a cél karakterlánca a kis-és nagybetűk megkülönböztetésével való összehasonlítást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e1b29-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="e1b29-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e1b29-112">EXAMPLES</span></span>

### <span data-ttu-id="e1b29-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1b29-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="e1b29-114">Felsorolja az összes olyan szolgáltatói erőforrástípust, amelyhez alias van telepítve.</span><span class="sxs-lookup"><span data-stu-id="e1b29-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="e1b29-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1b29-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="e1b29-116">Az összes szolgáltató erőforrás típusának felsorolása, az aliasokat nem tartalmazó nevekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="e1b29-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="e1b29-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="e1b29-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="e1b29-118">Felsorolja azokat a szolgáltatói erőforrás-típusokat, amelyek névtere megegyezik a "kiszámítás" értékkel, és tartalmaz egy aliast.</span><span class="sxs-lookup"><span data-stu-id="e1b29-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="e1b29-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="e1b29-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="e1b29-120">Felsorolja azokat a szolgáltatói erőforrásokat, amelyek erőforrás-típusa megegyezik a "virtuális" értékkel, és tartalmaz egy aliast.</span><span class="sxs-lookup"><span data-stu-id="e1b29-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="e1b29-121">Példa 5</span><span class="sxs-lookup"><span data-stu-id="e1b29-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="e1b29-122">Felsorolja az összes olyan szolgáltató erőforrás-típust, amelynek az erőforrás-típusa megegyezik a "virtuális" értékkel, az aliasok nélkül.</span><span class="sxs-lookup"><span data-stu-id="e1b29-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="e1b29-123">6. példa</span><span class="sxs-lookup"><span data-stu-id="e1b29-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="e1b29-124">Felsorolja azokat a szolgáltatói erőforrás-típusokat, amelyek névterében a "kiszámítás" és az erőforrás típusa megegyezik a "virtuális" értékkel, és aliast tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e1b29-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="e1b29-125">Megjegyzés: – a NamespaceMatch és a ResourceTypeMatch kizárólagos találatokat ad vissza, míg a többiek befogadók.</span><span class="sxs-lookup"><span data-stu-id="e1b29-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="e1b29-126">7. példa</span><span class="sxs-lookup"><span data-stu-id="e1b29-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="e1b29-127">A "virtuális" aliast tartalmazó összes szolgáltató-erőforrástípus felsorolása.</span><span class="sxs-lookup"><span data-stu-id="e1b29-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="e1b29-128">8. példa</span><span class="sxs-lookup"><span data-stu-id="e1b29-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="e1b29-129">A "virtuális" aliast tartalmazó összes szolgáltató erőforrástípus, vagy egy, az elérési út megfelelő "hálózattal" aliast tartalmazó lista.</span><span class="sxs-lookup"><span data-stu-id="e1b29-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="e1b29-130">Példa 9</span><span class="sxs-lookup"><span data-stu-id="e1b29-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="e1b29-131">Az alfa API-t tartalmazó összes szolgáltató erőforrástípus, vagy egy Alpha API-t tartalmazó aliast tartalmazó lista.</span><span class="sxs-lookup"><span data-stu-id="e1b29-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="e1b29-132">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1b29-132">PARAMETERS</span></span>

### <span data-ttu-id="e1b29-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="e1b29-133">-AliasMatch</span></span>
<span data-ttu-id="e1b29-134">A kimeneti elemek aliasokat tartalmazó elemei, akiknek a neve megegyezik az értékkel.</span><span class="sxs-lookup"><span data-stu-id="e1b29-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b29-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1b29-135">-ApiVersion</span></span>
<span data-ttu-id="e1b29-136">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1b29-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="e1b29-137">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e1b29-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="e1b29-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="e1b29-138">-ApiVersionMatch</span></span>
<span data-ttu-id="e1b29-139">Azon kimeneti elemek, amelyek erőforrás-típusa vagy aliasa megfelelő API-verzióval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e1b29-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="e1b29-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b29-140">-DefaultProfile</span></span>
<span data-ttu-id="e1b29-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1b29-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e1b29-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="e1b29-142">-ListAvailable</span></span>
<span data-ttu-id="e1b29-143">A kimeneti egyező elemek közé tartozik aliasok nélkül.</span><span class="sxs-lookup"><span data-stu-id="e1b29-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b29-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="e1b29-144">-LocationMatch</span></span>
<span data-ttu-id="e1b29-145">Azokat a kimeneti elemeket tartalmazza, amelyeknek az erőforrás-típusa megegyezik a megfelelő hellyel.</span><span class="sxs-lookup"><span data-stu-id="e1b29-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b29-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="e1b29-146">-NamespaceMatch</span></span>
<span data-ttu-id="e1b29-147">Korlátozza a kimenetet olyan elemek esetén, amelyek névtére megegyezik az adott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e1b29-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b29-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="e1b29-148">-PathMatch</span></span>
<span data-ttu-id="e1b29-149">A kimeneti elemek között az értéknek megfelelő elérési utat tartalmazó aliasokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e1b29-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b29-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="e1b29-150">-Pre</span></span>
<span data-ttu-id="e1b29-151">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e1b29-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="e1b29-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="e1b29-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="e1b29-153">Korlátozza a kimenetet olyan elemek esetén, amelyek erőforrás-típusa megegyezik az adott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e1b29-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b29-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b29-154">CommonParameters</span></span>
<span data-ttu-id="e1b29-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1b29-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b29-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1b29-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b29-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1b29-157">INPUTS</span></span>

### <span data-ttu-id="e1b29-158">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1b29-158">None</span></span>

## <span data-ttu-id="e1b29-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1b29-159">OUTPUTS</span></span>

### <span data-ttu-id="e1b29-160">Microsoft. Azure. Command. ResourceManager. parancsmagok. végrehajtás. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="e1b29-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="e1b29-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1b29-161">NOTES</span></span>

* <span data-ttu-id="e1b29-162">Az aliasok vagy bármely más tulajdonság kibontásához végezze el a kimenetet a kívánt értékre `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="e1b29-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="e1b29-163">Példa: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="e1b29-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="e1b29-164">A kimeneten további tulajdonságok is elérhetők, és a kimenetet a kimenetük segítségével is megjelenítheti `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="e1b29-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="e1b29-165">Példa: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="e1b29-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="e1b29-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1b29-166">RELATED LINKS</span></span>
