---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 2926aa351e7e9f1f9251c5a6e6a2292b27ef93b0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398189"
---
# <span data-ttu-id="8a691-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a691-101">Get-AzResource</span></span>

## <span data-ttu-id="8a691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a691-102">SYNOPSIS</span></span>

<span data-ttu-id="8a691-103">Erőforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="8a691-103">Gets resources.</span></span>

## <span data-ttu-id="8a691-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a691-104">SYNTAX</span></span>

### <span data-ttu-id="8a691-105">ByTagNameValueParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a691-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a691-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a691-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a691-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a691-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a691-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a691-108">DESCRIPTION</span></span>

<span data-ttu-id="8a691-109">A **Get-AzResource** parancsmag Azure-erőforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="8a691-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="8a691-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a691-110">EXAMPLES</span></span>

### <span data-ttu-id="8a691-111">1. példa: Az aktuális előfizetés összes erőforrásának lekérte</span><span class="sxs-lookup"><span data-stu-id="8a691-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="8a691-112">Ez a parancs az aktuális előfizetés összes erőforrását beveszi.</span><span class="sxs-lookup"><span data-stu-id="8a691-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="8a691-113">2. példa: Erőforráscsoport összes erőforrásának be szereznie</span><span class="sxs-lookup"><span data-stu-id="8a691-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="8a691-114">Ez a parancs a "testRG" erőforráscsoport összes erőforrását beveszi.</span><span class="sxs-lookup"><span data-stu-id="8a691-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="8a691-115">3. példa: Az összes olyan erőforrás lekérte, amelynek erőforráscsoportja megfelel a megadott helyettesítő karakternek</span><span class="sxs-lookup"><span data-stu-id="8a691-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8a691-116">Ez a parancs az összes olyan erőforrást beveszi, amelynek erőforráscsoportja a "más" szóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="8a691-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="8a691-117">4. példa: Az összes erőforrás lekérte egy megadott névvel</span><span class="sxs-lookup"><span data-stu-id="8a691-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="8a691-118">Ez a parancs az összes olyan erőforrást beveszi, amelynek az erőforrásneve "testVM".</span><span class="sxs-lookup"><span data-stu-id="8a691-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="8a691-119">5. példa: Az összes olyan erőforrás lekérte, amelynek a neve megegyezik a megadott helyettesítő karakterekkel</span><span class="sxs-lookup"><span data-stu-id="8a691-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8a691-120">Ez a parancs az összes olyan erőforrást beveszi, amelynek az erőforrásneve "teszt" névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="8a691-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="8a691-121">6. példa: Egy adott erőforrástípus összes erőforrásának lekérte</span><span class="sxs-lookup"><span data-stu-id="8a691-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8a691-122">Ez a parancs az aktuális előfizetések összes olyan erőforrását beveszi, amely virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="8a691-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="8a691-123">7. példa: Erőforrás lekérte erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8a691-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="8a691-124">Ez a parancs a megadott erőforrás-azonosítóval kapja meg az erőforrást, amely egy "testVM" nevű virtuális gép a "testRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8a691-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="8a691-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a691-125">PARAMETERS</span></span>

### <span data-ttu-id="8a691-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a691-126">-ApiVersion</span></span>

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

### <span data-ttu-id="8a691-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a691-127">-DefaultProfile</span></span>
<span data-ttu-id="8a691-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8a691-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a691-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="8a691-129">-ExpandProperties</span></span>
<span data-ttu-id="8a691-130">Ha meg van adva, kibontja az erőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="8a691-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="8a691-131">-Name</span><span class="sxs-lookup"><span data-stu-id="8a691-131">-Name</span></span>
<span data-ttu-id="8a691-132">A visszakeresni szükséges erőforrás(ak) neve.</span><span class="sxs-lookup"><span data-stu-id="8a691-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="8a691-133">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="8a691-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8a691-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8a691-134">-ODataQuery</span></span>

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

### <span data-ttu-id="8a691-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8a691-135">-Pre</span></span>

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

### <span data-ttu-id="8a691-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a691-136">-ResourceGroupName</span></span>
<span data-ttu-id="8a691-137">Az erőforráscsoport, amelybe a beolvasott erőforrás(k)t beolvassa.</span><span class="sxs-lookup"><span data-stu-id="8a691-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="8a691-138">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="8a691-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8a691-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a691-139">-ResourceId</span></span>
<span data-ttu-id="8a691-140">A teljes erőforrás-azonosítót adja meg, az alábbi példában megadottak szerint. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="8a691-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a691-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8a691-141">-ResourceType</span></span>
<span data-ttu-id="8a691-142">A visszakeresni szükséges erőforrás(ak) erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="8a691-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="8a691-143">Például: Microsoft.Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="8a691-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a691-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a691-144">-Tag</span></span>

<span data-ttu-id="8a691-145">A megadott Azure-címkével rendelkezik erőforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="8a691-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="8a691-146">Írjon be egy olyan kivonattáblát, amely tartalmazza a Név vagy a Név és az Érték billentyűt.</span><span class="sxs-lookup"><span data-stu-id="8a691-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="8a691-147">A helyettesítő karakterek nem támogatottak. A "címke" egy névérték-pár, amely az erőforrásokra és az erőforráscsoportokra alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="8a691-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="8a691-148">Címkék használatával kategorizálhatja az erőforrásokat, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokkal kapcsolatos jegyzeteket vagy megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="8a691-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="8a691-149">Ha címkét szeretne hozzáadni egy erőforráshoz, használja a New-AzResource vagy Set-AzResource címke paraméterét.</span><span class="sxs-lookup"><span data-stu-id="8a691-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="8a691-150">Előre definiált címke létrehozásához használja a New-AzTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8a691-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="8a691-151">Ha segítségre van szüksége a kivonattáblák Windows PowerShellben való futtatásához, futtassa a "Get-Help about_Hashtables" parancsot.</span><span class="sxs-lookup"><span data-stu-id="8a691-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a691-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="8a691-152">-TagName</span></span>
<span data-ttu-id="8a691-153">A visszakeresni szükséges erőforrások címkéje.</span><span class="sxs-lookup"><span data-stu-id="8a691-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a691-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="8a691-154">-TagValue</span></span>
<span data-ttu-id="8a691-155">A visszakeresni szükséges erőforrás(ak) címkében megadott érték.</span><span class="sxs-lookup"><span data-stu-id="8a691-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a691-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a691-156">CommonParameters</span></span>
<span data-ttu-id="8a691-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a691-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a691-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a691-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a691-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a691-159">INPUTS</span></span>

### <span data-ttu-id="8a691-160">System.String</span><span class="sxs-lookup"><span data-stu-id="8a691-160">System.String</span></span>

## <span data-ttu-id="8a691-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a691-161">OUTPUTS</span></span>

### <span data-ttu-id="8a691-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="8a691-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="8a691-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a691-163">NOTES</span></span>

## <span data-ttu-id="8a691-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a691-164">RELATED LINKS</span></span>


[<span data-ttu-id="8a691-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a691-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="8a691-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a691-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8a691-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a691-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="8a691-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="8a691-168">Set-AzResource</span></span>](./Set-AzResource.md)
