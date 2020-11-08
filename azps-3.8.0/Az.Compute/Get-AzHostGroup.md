---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 26030677743b95ebb11431118ccae8adf0b08bcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013683"
---
# <span data-ttu-id="a9b4c-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="a9b4c-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="a9b4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b4c-103">Beolvashatja vagy listázhatja az állomásokat.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-103">Get or list hosts.</span></span>

## <span data-ttu-id="a9b4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9b4c-104">SYNTAX</span></span>

### <span data-ttu-id="a9b4c-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9b4c-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9b4c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a9b4c-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9b4c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="a9b4c-108">Ez a parancsmag egy állomás-csoportot fog kapni.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="a9b4c-109">Ez a parancsmag az erőforráscsoport összes állomását is felsorolja, ha nem adja meg a Host Name (állomásnév) nevet.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="a9b4c-110">Ez a parancsmag az előfizetésben szereplő összes állomást is felsorolja, ha a csoport neve vagy az erőforráscsoport neve sem szerepel a csoportban.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="a9b4c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a9b4c-111">EXAMPLES</span></span>

### <span data-ttu-id="a9b4c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a9b4c-112">Example 1</span></span>
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

<span data-ttu-id="a9b4c-113">Ez a parancs egy állomás-csoportot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-113">This command returns a host group.</span></span>

### <span data-ttu-id="a9b4c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a9b4c-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="a9b4c-115">Ez a parancs a megadott erőforráscsoport összes Host-csoportját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="a9b4c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a9b4c-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="a9b4c-117">Ez a parancs az előfizetésben szereplő összes állomás-csoportot visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="a9b4c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9b4c-118">PARAMETERS</span></span>

### <span data-ttu-id="a9b4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b4c-119">-DefaultProfile</span></span>
<span data-ttu-id="a9b4c-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9b4c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9b4c-121">-Name</span></span>
<span data-ttu-id="a9b4c-122">A Host csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-122">The name of the host group.</span></span>

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

### <span data-ttu-id="a9b4c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b4c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9b4c-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a9b4c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b4c-125">-ResourceId</span></span>
<span data-ttu-id="a9b4c-126">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="a9b4c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b4c-127">CommonParameters</span></span>
<span data-ttu-id="a9b4c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9b4c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b4c-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a9b4c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b4c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9b4c-130">INPUTS</span></span>

### <span data-ttu-id="a9b4c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a9b4c-131">System.String</span></span>

## <span data-ttu-id="a9b4c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9b4c-132">OUTPUTS</span></span>

### <span data-ttu-id="a9b4c-133">Microsoft. Azure. commands. számítási. Automation. models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="a9b4c-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="a9b4c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9b4c-134">NOTES</span></span>

## <span data-ttu-id="a9b4c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9b4c-135">RELATED LINKS</span></span>
