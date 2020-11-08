---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185629"
---
# <span data-ttu-id="b01bc-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b01bc-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="b01bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b01bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b01bc-103">Az Azure elérhetőségi készleteit egy erőforráscsoport kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b01bc-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="b01bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b01bc-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b01bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b01bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b01bc-106">A **Get-AzAvailabilitySet** parancsmag az Azure elérhetőségi készleteit egy erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b01bc-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="b01bc-107">Megadhatja a beszerzéshez megadott elérhetőségi készlet nevét.</span><span class="sxs-lookup"><span data-stu-id="b01bc-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="b01bc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b01bc-108">EXAMPLES</span></span>

### <span data-ttu-id="b01bc-109">Példa 1: meghatározott elérhetőségi halmaz beszerzése</span><span class="sxs-lookup"><span data-stu-id="b01bc-109">Example 1: Get a specific availability set</span></span>
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

<span data-ttu-id="b01bc-110">Ez a parancs beolvassa a AvailabilitySet03 nevű ResourceGroup11 nevű erőforrás-csoport elérhetőségi készletét.</span><span class="sxs-lookup"><span data-stu-id="b01bc-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="b01bc-111">2. példa: az összes elérhetőségi készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="b01bc-111">Example 2: Get all availability sets</span></span>
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

<span data-ttu-id="b01bc-112">Ez a parancs a ResourceGroup11 nevű erőforráscsoport elérhetőségi készleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b01bc-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="b01bc-113">3. példa: az összes elérhetőségi halmaz beolvasása szűréssel</span><span class="sxs-lookup"><span data-stu-id="b01bc-113">Example 3: Get all availability sets with filtering</span></span>
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

<span data-ttu-id="b01bc-114">Ez a parancs a "AvailabilitySet0" kezdetű ResourceGroup11 nevű erőforráscsoport elérhetőségi készleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b01bc-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="b01bc-115">Példa 4: az összes elérhetőségi halmaz beszerzése a AvailabilitySet0 kezdődő névvel</span><span class="sxs-lookup"><span data-stu-id="b01bc-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
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

<span data-ttu-id="b01bc-116">Ez a parancs a "AvailabilitySet0" kezdetű elérhetőségi készleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b01bc-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="b01bc-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b01bc-117">PARAMETERS</span></span>

### <span data-ttu-id="b01bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01bc-118">-DefaultProfile</span></span>
<span data-ttu-id="b01bc-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b01bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01bc-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b01bc-120">-Name</span></span>
<span data-ttu-id="b01bc-121">A parancsmag által beolvasott elérhetőségi készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b01bc-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b01bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b01bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="b01bc-123">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b01bc-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b01bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01bc-124">CommonParameters</span></span>
<span data-ttu-id="b01bc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b01bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01bc-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b01bc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01bc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b01bc-127">INPUTS</span></span>

### <span data-ttu-id="b01bc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b01bc-128">System.String</span></span>

## <span data-ttu-id="b01bc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b01bc-129">OUTPUTS</span></span>

### <span data-ttu-id="b01bc-130">Microsoft. Azure. commands. kiszámítás. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b01bc-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="b01bc-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b01bc-131">NOTES</span></span>

## <span data-ttu-id="b01bc-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b01bc-132">RELATED LINKS</span></span>

[<span data-ttu-id="b01bc-133">Új – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b01bc-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="b01bc-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b01bc-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


