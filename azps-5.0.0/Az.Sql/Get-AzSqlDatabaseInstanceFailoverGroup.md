---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185668"
---
# <span data-ttu-id="f5261-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f5261-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="f5261-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5261-102">SYNOPSIS</span></span>
<span data-ttu-id="f5261-103">Beolvashatja vagy listázhatja a példány feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="f5261-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="f5261-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5261-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5261-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5261-105">DESCRIPTION</span></span>
<span data-ttu-id="f5261-106">Beolvassa a konkrét példány-feladatátvételi csoportot, vagy felsorolja a példány feladatátvételi csoportját a felhasználó előfizetése alá tartozó régióban.</span><span class="sxs-lookup"><span data-stu-id="f5261-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="f5261-107">A parancs végrehajtásához a példány-feladatátvételi csoport bármely területe használható.</span><span class="sxs-lookup"><span data-stu-id="f5261-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="f5261-108">A visszaadott értékek az adott régióban lévő felügyelt példányok állapotát tükrözik a példány-feladatátvételi csoporttal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="f5261-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="f5261-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5261-109">EXAMPLES</span></span>

### <span data-ttu-id="f5261-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5261-110">Example 1</span></span>
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

<span data-ttu-id="f5261-111">A régió összes feladatátvételi csoportjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="f5261-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="f5261-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f5261-112">Example 2</span></span>
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

<span data-ttu-id="f5261-113">Konkrét példány-feladatátvételi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="f5261-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="f5261-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5261-114">PARAMETERS</span></span>

### <span data-ttu-id="f5261-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5261-115">-DefaultProfile</span></span>
<span data-ttu-id="f5261-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5261-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5261-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="f5261-117">-Location</span></span>
<span data-ttu-id="f5261-118">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="f5261-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="f5261-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5261-119">-Name</span></span>
<span data-ttu-id="f5261-120">A lekérdezni kívánt példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5261-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="f5261-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5261-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5261-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5261-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5261-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5261-123">CommonParameters</span></span>
<span data-ttu-id="f5261-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5261-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5261-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5261-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5261-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5261-126">INPUTS</span></span>

### <span data-ttu-id="f5261-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f5261-127">System.String</span></span>

## <span data-ttu-id="f5261-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5261-128">OUTPUTS</span></span>

### <span data-ttu-id="f5261-129">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f5261-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="f5261-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5261-130">NOTES</span></span>

## <span data-ttu-id="f5261-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5261-131">RELATED LINKS</span></span>