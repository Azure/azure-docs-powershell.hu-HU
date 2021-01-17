---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480884"
---
# <span data-ttu-id="d8cc7-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8cc7-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="d8cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cc7-103">Az Azure rendelkezésre állási készleteket kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="d8cc7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8cc7-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8cc7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cc7-106">A **Get-AzAvailabilitySet** parancsmag az Azure rendelkezésre állási készletét kapja meg egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="d8cc7-107">Megadhatja egy lekért elérhetőségi készlet nevét.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="d8cc7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8cc7-108">EXAMPLES</span></span>

### <span data-ttu-id="d8cc7-109">1. példa: Adott elérhetőségi készlet lekérte</span><span class="sxs-lookup"><span data-stu-id="d8cc7-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d8cc7-110">Ez a parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d8cc7-111">2. példa: Az összes rendelkezésre állási készlet lekérte</span><span class="sxs-lookup"><span data-stu-id="d8cc7-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d8cc7-112">Ez a parancs az Erőforráscsoport11 nevű erőforráscsoport összes rendelkezésre állási csoportját beállítja.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d8cc7-113">3. példa: Az összes rendelkezésre állási készlet lekérte a szűrést</span><span class="sxs-lookup"><span data-stu-id="d8cc7-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d8cc7-114">Ez a parancs az Erőforráscsoport11 nevű erőforráscsoport összes rendelkezésre állási csoportját az "ElérhetőségIKészlet0" kezdetűre állítja.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="d8cc7-115">4. példa: Az összes rendelkezésre állási készlet lekért neve az ElérhetőségIet0 névvel kezdve</span><span class="sxs-lookup"><span data-stu-id="d8cc7-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="d8cc7-116">Ez a parancs a "AvailabilitySet0" kezdettől indulva beállítja az összes rendelkezésre állási készletet.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="d8cc7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8cc7-117">PARAMETERS</span></span>

### <span data-ttu-id="d8cc7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cc7-118">-DefaultProfile</span></span>
<span data-ttu-id="d8cc7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8cc7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d8cc7-120">-Name</span></span>
<span data-ttu-id="d8cc7-121">Megadja annak az elérhetőségi készletnek a nevét, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d8cc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8cc7-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d8cc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cc7-124">CommonParameters</span></span>
<span data-ttu-id="d8cc7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cc7-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8cc7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cc7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8cc7-127">INPUTS</span></span>

### <span data-ttu-id="d8cc7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d8cc7-128">System.String</span></span>

## <span data-ttu-id="d8cc7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8cc7-129">OUTPUTS</span></span>

### <span data-ttu-id="d8cc7-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8cc7-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d8cc7-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8cc7-131">NOTES</span></span>

## <span data-ttu-id="d8cc7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8cc7-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8cc7-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8cc7-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="d8cc7-134">Remove-AzavailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8cc7-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


