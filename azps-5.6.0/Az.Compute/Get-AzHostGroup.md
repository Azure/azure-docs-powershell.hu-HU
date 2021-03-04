---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 1b33803ff3a33897d46519952db99ceda1b12c99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938889"
---
# <span data-ttu-id="0bdbd-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="0bdbd-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="0bdbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="0bdbd-103">Állomások le- vagy listába való be- vagy listába való be- vagy list</span><span class="sxs-lookup"><span data-stu-id="0bdbd-103">Get or list hosts.</span></span>

## <span data-ttu-id="0bdbd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0bdbd-104">SYNTAX</span></span>

### <span data-ttu-id="0bdbd-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0bdbd-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bdbd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0bdbd-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bdbd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0bdbd-107">DESCRIPTION</span></span>
<span data-ttu-id="0bdbd-108">Ez a parancsmag állomáscsoportot fog kapni.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="0bdbd-109">Ez a parancsmag felsorolja az erőforráscsoportok összes állomáscsoportját is, ha nem ad meg állomáscsoportnevet.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="0bdbd-110">Ez a parancsmag felsorolja az előfizetés összes állomáscsoportját is, ha sem az állomáscsoport, sem az erőforráscsoport neve nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="0bdbd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0bdbd-111">EXAMPLES</span></span>

### <span data-ttu-id="0bdbd-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0bdbd-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="0bdbd-113">Ez a parancs állomáscsoportot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-113">This command returns a host group.</span></span>

### <span data-ttu-id="0bdbd-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0bdbd-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="0bdbd-115">Ez a parancs a megadott erőforráscsoport összes állomáscsoportját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="0bdbd-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="0bdbd-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="0bdbd-117">Ez a parancs az előfizetés összes állomáscsoportját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="0bdbd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bdbd-118">PARAMETERS</span></span>

### <span data-ttu-id="0bdbd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bdbd-119">-DefaultProfile</span></span>
<span data-ttu-id="0bdbd-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bdbd-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="0bdbd-121">-InstanceView</span></span>
<span data-ttu-id="0bdbd-122">Bontsa ki a visszaadott objektumot úgy, hogy az állomás példánynézetét is listába sorolja.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bdbd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0bdbd-123">-Name</span></span>
<span data-ttu-id="0bdbd-124">A gazdacsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bdbd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bdbd-125">-ResourceGroupName</span></span>
<span data-ttu-id="0bdbd-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bdbd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bdbd-127">-ResourceId</span></span>
<span data-ttu-id="0bdbd-128">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="0bdbd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bdbd-129">CommonParameters</span></span>
<span data-ttu-id="0bdbd-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bdbd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bdbd-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bdbd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bdbd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bdbd-132">INPUTS</span></span>

### <span data-ttu-id="0bdbd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0bdbd-133">System.String</span></span>

## <span data-ttu-id="0bdbd-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bdbd-134">OUTPUTS</span></span>

### <span data-ttu-id="0bdbd-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="0bdbd-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="0bdbd-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0bdbd-136">NOTES</span></span>

## <span data-ttu-id="0bdbd-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bdbd-137">RELATED LINKS</span></span>
