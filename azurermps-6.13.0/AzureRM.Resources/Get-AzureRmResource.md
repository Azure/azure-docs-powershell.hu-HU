---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 7b18a2f5a030a71de0604604b86ba71d2dbe6e03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672455"
---
# <span data-ttu-id="d3f7f-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3f7f-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="d3f7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3f7f-102">SYNOPSIS</span></span>

<span data-ttu-id="d3f7f-103">Erőforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3f7f-104">SYNTAX</span></span>

### <span data-ttu-id="d3f7f-105">ByTagNameValueParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3f7f-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-TagName <String>] [-TagValue <String>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f7f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f7f-106">ByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f7f-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f7f-107">ByTagObjectParameterSet</span></span>
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f7f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3f7f-108">DESCRIPTION</span></span>

<span data-ttu-id="d3f7f-109">A **Get-AzureRmResource** parancsmag Azure-erőforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-109">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="d3f7f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d3f7f-110">EXAMPLES</span></span>

### <span data-ttu-id="d3f7f-111">Példa 1: a jelenlegi előfizetés összes erőforrásának lekérése</span><span class="sxs-lookup"><span data-stu-id="d3f7f-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzureRmResource | ft

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

<span data-ttu-id="d3f7f-112">Ez a parancs a jelenlegi előfizetés összes erőforrását megkapja.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="d3f7f-113">2. példa: erőforráscsoport erőforrásainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="d3f7f-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzureRmResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="d3f7f-114">Ez a parancs a "testRG" erőforráscsoport összes erőforrását megkapja.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="d3f7f-115">3. példa: az összes olyan erőforrás beszerzése, amelynek az erőforráscsoport megegyezik a megadott helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="d3f7f-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzureRmResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="d3f7f-116">Ez a parancs azokat az erőforrásokat kapja meg, amelyek erőforráscsoport az "egyéb" csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="d3f7f-117">Példa 4: az összes erőforrás beolvasása egy adott névvel</span><span class="sxs-lookup"><span data-stu-id="d3f7f-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzureRmResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="d3f7f-118">Ez a parancs minden olyan erőforrást visszanyer, amelynek az erőforrás neve "testVM".</span><span class="sxs-lookup"><span data-stu-id="d3f7f-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="d3f7f-119">Példa 5: az összes olyan erőforrás lekérése, akinek a neve megegyezik a megadott helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="d3f7f-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzureRmResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="d3f7f-120">Ez a parancs minden olyan erőforrást beolvas, amelynek az erőforrás neve "teszt"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="d3f7f-121">Példa 6: adott erőforrástípus összes erőforrásának lekérése</span><span class="sxs-lookup"><span data-stu-id="d3f7f-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="d3f7f-122">Ez a parancs a virtuális gépek jelenlegi előfizetésében található összes erőforrást megkapja.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="d3f7f-123">7. példa: erőforrás-erőforrás-azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3f7f-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzureRmResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="d3f7f-124">Ez a parancs az erőforrást a megadott erőforrás-azonosítóval kapja meg, amely a "testRG" erőforráscsoport "testVM" nevű virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="d3f7f-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3f7f-125">PARAMETERS</span></span>

### <span data-ttu-id="d3f7f-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d3f7f-126">-ApiVersion</span></span>

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

### <span data-ttu-id="d3f7f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f7f-127">-DefaultProfile</span></span>
<span data-ttu-id="d3f7f-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d3f7f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f7f-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="d3f7f-129">-ExpandProperties</span></span>
<span data-ttu-id="d3f7f-130">Ha meg van adva, kibontja az erőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="d3f7f-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3f7f-131">-Name</span></span>
<span data-ttu-id="d3f7f-132">A beolvasni kívánt erőforrás (ok) neve.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="d3f7f-133">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f7f-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d3f7f-134">-ODataQuery</span></span>

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

### <span data-ttu-id="d3f7f-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="d3f7f-135">-Pre</span></span>

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

### <span data-ttu-id="d3f7f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f7f-136">-ResourceGroupName</span></span>
<span data-ttu-id="d3f7f-137">Az erőforráscsoport a retireved erőforrás (oka) t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-137">The resource group the resource(s) that is retireved belongs in.</span></span> <span data-ttu-id="d3f7f-138">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="d3f7f-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f7f-139">-ResourceId</span></span>
<span data-ttu-id="d3f7f-140">A teljesen minősített erőforrás AZONOSÍTÓját adja meg, az alábbi példában látható módon. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="d3f7f-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="d3f7f-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d3f7f-141">-ResourceType</span></span>
<span data-ttu-id="d3f7f-142">A beolvasandó erőforrás (ok) erőforrás-típusa.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="d3f7f-143">Példa: Microsoft. számítási/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="d3f7f-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="d3f7f-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="d3f7f-144">-Tag</span></span>

<span data-ttu-id="d3f7f-145">A megadott Azure címkét tartalmazó erőforrásokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="d3f7f-146">Írjon be egy, a név vagy a név és az érték kulcsú hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="d3f7f-147">A helyettesítő karakterek használata nem támogatott. A "címke" egy olyan név-érték páros, amelyet az erőforrásokra és az erőforrás-csoportokra lehet alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="d3f7f-148">Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="d3f7f-149">Ha hozzá szeretne adni egy címkét egy erőforráshoz, használja az New-AzureRmResource vagy Set-AzureRmResource parancsmagok címke paraméterét.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-149">To add a tag to a resource, use the Tag parameter of the New-AzureRmResource or Set-AzureRmResource cmdlets.</span></span> <span data-ttu-id="d3f7f-150">Ha előre definiált címkét szeretne létrehozni, használja az New-AzureRmTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-150">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span> <span data-ttu-id="d3f7f-151">Ha segítségre van szüksége a Windows PowerShell kivonatoló tábláihoz, futtassa a "Get-Help about_Hashtables" parancsot.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="d3f7f-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="d3f7f-152">-TagName</span></span>
<span data-ttu-id="d3f7f-153">A beolvasni kívánt erőforrás (ok) címkéjének a kulcsa.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="d3f7f-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="d3f7f-154">-TagValue</span></span>
<span data-ttu-id="d3f7f-155">A beolvasandó erőforrás (ok) címke értéke.</span><span class="sxs-lookup"><span data-stu-id="d3f7f-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="d3f7f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f7f-156">CommonParameters</span></span>
<span data-ttu-id="d3f7f-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3f7f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f7f-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f7f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f7f-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3f7f-159">INPUTS</span></span>

### <span data-ttu-id="d3f7f-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3f7f-160">None</span></span>

## <span data-ttu-id="d3f7f-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3f7f-161">OUTPUTS</span></span>

### <span data-ttu-id="d3f7f-162">Microsoft. Azure. Command. ResourceManagement. models. PSResource</span><span class="sxs-lookup"><span data-stu-id="d3f7f-162">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="d3f7f-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3f7f-163">NOTES</span></span>

## <span data-ttu-id="d3f7f-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3f7f-164">RELATED LINKS</span></span>

[<span data-ttu-id="d3f7f-165">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3f7f-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="d3f7f-166">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3f7f-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="d3f7f-167">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3f7f-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="d3f7f-168">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3f7f-168">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="d3f7f-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3f7f-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
