---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: d1790f3525e63890d164db1a62903026be4f483a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938890"
---
# <span data-ttu-id="897cf-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="897cf-101">Get-AzHost</span></span>

## <span data-ttu-id="897cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="897cf-102">SYNOPSIS</span></span>
<span data-ttu-id="897cf-103">Állomások le- vagy listába való be- vagy listába való be- vagy list</span><span class="sxs-lookup"><span data-stu-id="897cf-103">Get or list hosts.</span></span>

## <span data-ttu-id="897cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="897cf-104">SYNTAX</span></span>

### <span data-ttu-id="897cf-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="897cf-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="897cf-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="897cf-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="897cf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="897cf-107">DESCRIPTION</span></span>
<span data-ttu-id="897cf-108">Ez a parancsmag állomást fog kapni egy gazdacsoportban.</span><span class="sxs-lookup"><span data-stu-id="897cf-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="897cf-109">Ez a parancsmag felsorolja az állomáscsoport összes állomását is, ha nem ad meg állomásnevet.</span><span class="sxs-lookup"><span data-stu-id="897cf-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="897cf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="897cf-110">EXAMPLES</span></span>

### <span data-ttu-id="897cf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="897cf-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="897cf-112">Ez a parancs egy állomást ad vissza.</span><span class="sxs-lookup"><span data-stu-id="897cf-112">This command returns a host.</span></span>

### <span data-ttu-id="897cf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="897cf-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="897cf-114">Ez a parancs egy állomás példánynézetét adja vissza.</span><span class="sxs-lookup"><span data-stu-id="897cf-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="897cf-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="897cf-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="897cf-116">Ez a parancs az adott gazdacsoport összes állomását visszaadja.</span><span class="sxs-lookup"><span data-stu-id="897cf-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="897cf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="897cf-117">PARAMETERS</span></span>

### <span data-ttu-id="897cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897cf-118">-DefaultProfile</span></span>
<span data-ttu-id="897cf-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="897cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897cf-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="897cf-120">-HostGroupName</span></span>
<span data-ttu-id="897cf-121">A gazdacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="897cf-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="897cf-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="897cf-122">-InstanceView</span></span>
<span data-ttu-id="897cf-123">Azt jelzi, hogy ez a parancsmag csak az állomás példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="897cf-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

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

### <span data-ttu-id="897cf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="897cf-124">-Name</span></span>
<span data-ttu-id="897cf-125">Az állomás neve.</span><span class="sxs-lookup"><span data-stu-id="897cf-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="897cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="897cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="897cf-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="897cf-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="897cf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="897cf-128">-ResourceId</span></span>
<span data-ttu-id="897cf-129">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="897cf-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="897cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897cf-130">CommonParameters</span></span>
<span data-ttu-id="897cf-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897cf-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="897cf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897cf-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="897cf-133">INPUTS</span></span>

### <span data-ttu-id="897cf-134">System.String</span><span class="sxs-lookup"><span data-stu-id="897cf-134">System.String</span></span>

## <span data-ttu-id="897cf-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="897cf-135">OUTPUTS</span></span>

### <span data-ttu-id="897cf-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="897cf-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="897cf-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="897cf-137">NOTES</span></span>

## <span data-ttu-id="897cf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="897cf-138">RELATED LINKS</span></span>
