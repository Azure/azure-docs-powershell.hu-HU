---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: dbb0cb56c50025e6b257d801957b1a75479220f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839245"
---
# <span data-ttu-id="708b3-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708b3-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="708b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="708b3-102">SYNOPSIS</span></span>
<span data-ttu-id="708b3-103">Beolvashatja vagy listázhatja a példány feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="708b3-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="708b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="708b3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="708b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="708b3-105">DESCRIPTION</span></span>
<span data-ttu-id="708b3-106">Beolvassa a konkrét példány-feladatátvételi csoportot, vagy felsorolja a példány feladatátvételi csoportját a felhasználó előfizetése alá tartozó régióban.</span><span class="sxs-lookup"><span data-stu-id="708b3-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="708b3-107">A parancs végrehajtásához a példány-feladatátvételi csoport bármely területe használható.</span><span class="sxs-lookup"><span data-stu-id="708b3-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="708b3-108">A visszaadott értékek az adott régióban lévő felügyelt példányok állapotát tükrözik a példány-feladatátvételi csoporttal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="708b3-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="708b3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="708b3-109">EXAMPLES</span></span>

### <span data-ttu-id="708b3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="708b3-110">Example 1</span></span>
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

<span data-ttu-id="708b3-111">A régió összes feladatátvételi csoportjának felsorolása</span><span class="sxs-lookup"><span data-stu-id="708b3-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="708b3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="708b3-112">Example 2</span></span>
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

<span data-ttu-id="708b3-113">Konkrét példány-feladatátvételi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="708b3-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="708b3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="708b3-114">PARAMETERS</span></span>

### <span data-ttu-id="708b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708b3-115">-DefaultProfile</span></span>
<span data-ttu-id="708b3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="708b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708b3-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="708b3-117">-Location</span></span>
<span data-ttu-id="708b3-118">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="708b3-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708b3-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="708b3-119">-Name</span></span>
<span data-ttu-id="708b3-120">A lekérdezni kívánt példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="708b3-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708b3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708b3-121">-ResourceGroupName</span></span>
<span data-ttu-id="708b3-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="708b3-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708b3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708b3-123">CommonParameters</span></span>
<span data-ttu-id="708b3-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="708b3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708b3-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="708b3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708b3-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="708b3-126">INPUTS</span></span>

### <span data-ttu-id="708b3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="708b3-127">System.String</span></span>

## <span data-ttu-id="708b3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="708b3-128">OUTPUTS</span></span>

### <span data-ttu-id="708b3-129">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="708b3-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="708b3-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="708b3-130">NOTES</span></span>

## <span data-ttu-id="708b3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="708b3-131">RELATED LINKS</span></span>
