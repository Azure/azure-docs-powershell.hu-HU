---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018135"
---
# <span data-ttu-id="6bded-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="6bded-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="6bded-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6bded-102">SYNOPSIS</span></span>
<span data-ttu-id="6bded-103">Beolvashatja vagy listázhatja az állomásokat.</span><span class="sxs-lookup"><span data-stu-id="6bded-103">Get or list hosts.</span></span>

## <span data-ttu-id="6bded-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6bded-104">SYNTAX</span></span>

### <span data-ttu-id="6bded-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bded-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bded-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6bded-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bded-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6bded-107">DESCRIPTION</span></span>
<span data-ttu-id="6bded-108">Ez a parancsmag egy állomás-csoportot fog kapni.</span><span class="sxs-lookup"><span data-stu-id="6bded-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="6bded-109">Ez a parancsmag az erőforráscsoport összes állomását is felsorolja, ha nem adja meg a Host Name (állomásnév) nevet.</span><span class="sxs-lookup"><span data-stu-id="6bded-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="6bded-110">Ez a parancsmag az előfizetésben szereplő összes állomást is felsorolja, ha a csoport neve vagy az erőforráscsoport neve sem szerepel a csoportban.</span><span class="sxs-lookup"><span data-stu-id="6bded-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="6bded-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6bded-111">EXAMPLES</span></span>

### <span data-ttu-id="6bded-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6bded-112">Example 1</span></span>
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

<span data-ttu-id="6bded-113">Ez a parancs egy állomás-csoportot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="6bded-113">This command returns a host group.</span></span>

### <span data-ttu-id="6bded-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="6bded-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="6bded-115">Ez a parancs a megadott erőforráscsoport összes Host-csoportját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="6bded-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="6bded-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="6bded-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="6bded-117">Ez a parancs az előfizetésben szereplő összes állomás-csoportot visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="6bded-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="6bded-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6bded-118">PARAMETERS</span></span>

### <span data-ttu-id="6bded-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bded-119">-DefaultProfile</span></span>
<span data-ttu-id="6bded-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bded-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bded-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="6bded-121">-InstanceView</span></span>
<span data-ttu-id="6bded-122">Bontsa ki a visszaadott objektumot az állomás példányának nézeteit is felsorolva.</span><span class="sxs-lookup"><span data-stu-id="6bded-122">Expand the returned object to also list the host's instance views.</span></span> 

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

### <span data-ttu-id="6bded-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6bded-123">-Name</span></span>
<span data-ttu-id="6bded-124">A Host csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6bded-124">The name of the host group.</span></span>

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

### <span data-ttu-id="6bded-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bded-125">-ResourceGroupName</span></span>
<span data-ttu-id="6bded-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6bded-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="6bded-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bded-127">-ResourceId</span></span>
<span data-ttu-id="6bded-128">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6bded-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="6bded-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bded-129">CommonParameters</span></span>
<span data-ttu-id="6bded-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6bded-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bded-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6bded-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bded-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bded-132">INPUTS</span></span>

### <span data-ttu-id="6bded-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6bded-133">System.String</span></span>

## <span data-ttu-id="6bded-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bded-134">OUTPUTS</span></span>

### <span data-ttu-id="6bded-135">Microsoft. Azure. commands. számítási. Automation. models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="6bded-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="6bded-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6bded-136">NOTES</span></span>

## <span data-ttu-id="6bded-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bded-137">RELATED LINKS</span></span>
