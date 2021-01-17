---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465943"
---
# <span data-ttu-id="2dc72-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2dc72-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="2dc72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dc72-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc72-103">Példány feladatátvételi csoportjait kapja meg vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="2dc72-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="2dc72-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2dc72-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc72-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2dc72-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc72-106">Egy adott feladatátvételi csoportot kap, vagy felsorolja a felhasználó előfizetése alatti régió példány-feladatátvételi csoportjait.</span><span class="sxs-lookup"><span data-stu-id="2dc72-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="2dc72-107">A példány feladatátvételi csoportjának bármelyik régiója használható a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="2dc72-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="2dc72-108">A visszaadott értékek az adott régió felügyelt példányainak állapotát tükrözik a Példány feladatátvétele csoporttal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="2dc72-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="2dc72-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2dc72-109">EXAMPLES</span></span>

### <span data-ttu-id="2dc72-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2dc72-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
    ResourceGroupName                     : rg
    Location                              : East US
    Name                                  : fg
    PartnerResourceGroupName              : rg
    PartnerRegion                         : West US
    PrimaryManagedInstanceName            : managedInstance1
    PartnerManagedInstanceName            : managedInstance2
    ReplicationRole                       : Primary
    ReplicationState                      : CATCH_UP
    ReadWriteFailoverPolicy               : Automatic
    FailoverWithDataLossGracePeriodHours  : 1
    ReadOnlyFailoverPolicy                : Disabled
    Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
}
```

<span data-ttu-id="2dc72-111">A régió összes feladatátvételi csoportja</span><span class="sxs-lookup"><span data-stu-id="2dc72-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="2dc72-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="2dc72-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="2dc72-113">Adott példány feladatátvételi csoportjának levétele</span><span class="sxs-lookup"><span data-stu-id="2dc72-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="2dc72-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dc72-114">PARAMETERS</span></span>

### <span data-ttu-id="2dc72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc72-115">-DefaultProfile</span></span>
<span data-ttu-id="2dc72-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2dc72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dc72-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2dc72-117">-Location</span></span>
<span data-ttu-id="2dc72-118">Annak a helyi régiónak a neve, amelyből lekéri a példány feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="2dc72-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc72-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2dc72-119">-Name</span></span>
<span data-ttu-id="2dc72-120">A lekért Példány feladatátvétele csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2dc72-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc72-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc72-121">-ResourceGroupName</span></span>
<span data-ttu-id="2dc72-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2dc72-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc72-123">CommonParameters</span></span>
<span data-ttu-id="2dc72-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc72-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dc72-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc72-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dc72-126">INPUTS</span></span>

### <span data-ttu-id="2dc72-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2dc72-127">System.String</span></span>

## <span data-ttu-id="2dc72-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dc72-128">OUTPUTS</span></span>

### <span data-ttu-id="2dc72-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="2dc72-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="2dc72-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2dc72-130">NOTES</span></span>

## <span data-ttu-id="2dc72-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2dc72-131">RELATED LINKS</span></span>
