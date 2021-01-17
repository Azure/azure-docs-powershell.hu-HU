---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 99be70e225dd607c580c4571f4ae332e7badf33a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480323"
---
# <span data-ttu-id="9d53c-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9d53c-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="9d53c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d53c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d53c-103">Ez a parancs létrehoz egy új Azure SQL-adatbázispéldány feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="9d53c-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="9d53c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d53c-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d53c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d53c-105">DESCRIPTION</span></span>
<span data-ttu-id="9d53c-106">Létrehoz egy új Azure SQL-adatbázis-példány feladatátvételi csoportot a megadott régiók között, a feljegyzett Felügyelt példány párral.</span><span class="sxs-lookup"><span data-stu-id="9d53c-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="9d53c-107">A Name.SqlDatabaseDnsSuffix (például az Name.database.windows.net) és a Name.secondary.SqlDatabaseDnsSuffix fájlban két Azure SQL-adatbázis TDS-végpont jön létre.</span><span class="sxs-lookup"><span data-stu-id="9d53c-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="9d53c-108">Ezek a végpontok a feladatátvételi csoport elsődleges és másodlagos régióihoz való csatlakozásra használhatók.</span><span class="sxs-lookup"><span data-stu-id="9d53c-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="9d53c-109">Ha az elsődleges régiót egy kimaradás érinti, a végpontok és adatbázisok automatikus feladatátvételét a rendszer a példány feladatátvételi csoportjának feladatátvételi házirendjéből és türelmi időszakából fogja kiválteni.</span><span class="sxs-lookup"><span data-stu-id="9d53c-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="9d53c-110">A "-GracePeriodWithDataLossHours" paraméter csak az 1 óránál nem kisebb értékeket támogatja a Példány feladatátvételi csoportok funkció előzetes verziója esetén.</span><span class="sxs-lookup"><span data-stu-id="9d53c-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="9d53c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d53c-111">EXAMPLES</span></span>

### <span data-ttu-id="9d53c-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9d53c-112">Example 1</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
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

<span data-ttu-id="9d53c-113">Ez a parancs létrehoz egy új feladatátvételi csoportot a Felügyelt példány pár "Automatikus" feladatátvételi házirendjával.</span><span class="sxs-lookup"><span data-stu-id="9d53c-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="9d53c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9d53c-114">Example 2</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
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
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="9d53c-115">Ez a parancs létrehoz egy új feladatátvételi csoportot a Felügyelt példány pár "Manuális" feladatátvételi házirendjával.</span><span class="sxs-lookup"><span data-stu-id="9d53c-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="9d53c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9d53c-116">Example 3</span></span>

<span data-ttu-id="9d53c-117">Ez a parancs létrehoz egy új Azure SQL-adatbázispéldány feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="9d53c-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="9d53c-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="9d53c-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="9d53c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d53c-119">PARAMETERS</span></span>

### <span data-ttu-id="9d53c-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="9d53c-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="9d53c-121">A másodlagos kiszolgálón kimaradás esetén automatikus feladatátvételt kell-e kiváltanunk az írásra elérhető végponton.</span><span class="sxs-lookup"><span data-stu-id="9d53c-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="9d53c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d53c-122">-DefaultProfile</span></span>
<span data-ttu-id="9d53c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d53c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d53c-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="9d53c-124">-FailoverPolicy</span></span>
<span data-ttu-id="9d53c-125">A példány feladatátvételi csoportjának feladatátvételi házirende.</span><span class="sxs-lookup"><span data-stu-id="9d53c-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9d53c-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="9d53c-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="9d53c-127">Az automatikus feladatátvétel kezdeményezésének időköze, ha kimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem fejezhető be adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="9d53c-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d53c-128">-Location</span><span class="sxs-lookup"><span data-stu-id="9d53c-128">-Location</span></span>
<span data-ttu-id="9d53c-129">Annak a helyi régiónak a neve, amelyből lekéri a példány feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="9d53c-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9d53c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9d53c-130">-Name</span></span>
<span data-ttu-id="9d53c-131">A létrehozni szükséges Azure SQL-adatbázis feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d53c-131">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d53c-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="9d53c-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="9d53c-133">Annak a felügyelt példánynak a neve a partner régiójában, amely hozzá lesz adva a Példány feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="9d53c-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d53c-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="9d53c-134">-PartnerRegion</span></span>
<span data-ttu-id="9d53c-135">A Példány feladatátvétele csoport partner régiójának neve.</span><span class="sxs-lookup"><span data-stu-id="9d53c-135">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d53c-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d53c-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="9d53c-137">A Példány feladatátvétele csoport másodlagos erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="9d53c-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9d53c-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d53c-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="9d53c-139">A példány feladatátvételi csoportjának másodlagos felügyelt példányának előfizetés-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9d53c-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="9d53c-140">Ez a paraméter csak az előfizetések közötti beállításhoz szükséges.</span><span class="sxs-lookup"><span data-stu-id="9d53c-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="9d53c-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="9d53c-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="9d53c-142">Annak a felügyelt példánynak a neve a helyi régióban, amely hozzá lesz adva a Példány feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="9d53c-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d53c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d53c-143">-ResourceGroupName</span></span>
<span data-ttu-id="9d53c-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9d53c-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="9d53c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d53c-145">-Confirm</span></span>
<span data-ttu-id="9d53c-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9d53c-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d53c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d53c-147">-WhatIf</span></span>
<span data-ttu-id="9d53c-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9d53c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d53c-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d53c-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d53c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d53c-150">CommonParameters</span></span>
<span data-ttu-id="9d53c-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d53c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d53c-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d53c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d53c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d53c-153">INPUTS</span></span>

### <span data-ttu-id="9d53c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="9d53c-154">System.String</span></span>

## <span data-ttu-id="9d53c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d53c-155">OUTPUTS</span></span>

### <span data-ttu-id="9d53c-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9d53c-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="9d53c-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d53c-157">NOTES</span></span>

## <span data-ttu-id="9d53c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d53c-158">RELATED LINKS</span></span>
