---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 04ed033559abe6fe6a60922f7b11a498ff4026bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839420"
---
# <span data-ttu-id="ac43e-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ac43e-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="ac43e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac43e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac43e-103">Ezzel a paranccsal létrehoz egy új Azure SQL-adatbázis-példány feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="ac43e-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="ac43e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac43e-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup -Name <String> [-PartnerResourceGroupName <String>] [-PartnerSubscriptionId <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac43e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac43e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac43e-106">Új Azure SQL adatbázis-példány feladatátvételi csoportot hoz létre a megadott régiók között, a megjelenő kezelt példány párral.</span><span class="sxs-lookup"><span data-stu-id="ac43e-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="ac43e-107">Két Azure SQL-adatbázis TDS-végpontokat a name. SqlDatabaseDnsSuffix (például Name.database.windows.net) és a name. középfokú. SqlDatabaseDnsSuffix függvény hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ac43e-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="ac43e-108">Ezek a végpontok akkor használhatók, amikor a feladatátvételi csoport elsődleges és másodlagos területéhez csatlakoznak.</span><span class="sxs-lookup"><span data-stu-id="ac43e-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="ac43e-109">Ha az elsődleges régiót áramkimaradás okozta, a végpontok és adatbázisok automatikus feladatátvételét a program a példa feladatátvételi házirend és a türelmi időszak által diktált módon indítja el.</span><span class="sxs-lookup"><span data-stu-id="ac43e-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="ac43e-110">A példány feladatátvételi csoportjai funkció előnézete során a '-GracePeriodWithDataLossHours ' paraméterben csak az 1 óránál nagyobb vagy azzal egyenlő értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="ac43e-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="ac43e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ac43e-111">EXAMPLES</span></span>

### <span data-ttu-id="ac43e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac43e-112">Example 1</span></span>
```
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

<span data-ttu-id="ac43e-113">Ez a parancs létrehoz egy új példány-feladatátvételi csoportot, amelyen a felügyelt példányok párosításához a feladatátvételi házirend "automatikus" érték látható.</span><span class="sxs-lookup"><span data-stu-id="ac43e-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="ac43e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ac43e-114">Example 2</span></span>
```
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

<span data-ttu-id="ac43e-115">Ez a parancs létrehoz egy új példány-feladatátvételi csoportot, amelyen a felügyelt példányok párosítása "kézi" a feladatátvételi házirendben szerepel.</span><span class="sxs-lookup"><span data-stu-id="ac43e-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="ac43e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac43e-116">PARAMETERS</span></span>

### <span data-ttu-id="ac43e-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="ac43e-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="ac43e-118">Azt, hogy a másodlagos kiszolgálón lévő leállás esetén az írásvédett végpont automatikus feladatátvételét kell-e elindítani.</span><span class="sxs-lookup"><span data-stu-id="ac43e-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="ac43e-119">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="ac43e-119">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac43e-120">-DefaultProfile</span></span>
<span data-ttu-id="ac43e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac43e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac43e-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ac43e-122">-FailoverPolicy</span></span>
<span data-ttu-id="ac43e-123">A példány-feladatátvételi csoport feladatátvételi házirendje.</span><span class="sxs-lookup"><span data-stu-id="ac43e-123">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="ac43e-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="ac43e-125">Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem hajtható végre adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="ac43e-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="ac43e-126">-Location</span></span>
<span data-ttu-id="ac43e-127">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="ac43e-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ac43e-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac43e-128">-Name</span></span>
<span data-ttu-id="ac43e-129">A létrehozandó Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac43e-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-130">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="ac43e-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="ac43e-131">A partnervállalat által a példány-feladatátvétel csoportba felvenni kívánt felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="ac43e-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="ac43e-132">-PartnerRegion</span></span>
<span data-ttu-id="ac43e-133">A példány feladatátvétele csoport partner területének neve.</span><span class="sxs-lookup"><span data-stu-id="ac43e-133">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac43e-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ac43e-135">A példány-feladatátvételi csoport másodlagos erőforrás csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="ac43e-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-136">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac43e-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="ac43e-137">A példány feladatátvétele csoport másodlagos felügyelt példányának előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac43e-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="ac43e-138">Ez a paraméter csak a több előfizetés beállításához szükséges</span><span class="sxs-lookup"><span data-stu-id="ac43e-138">This parameter is only needed for cross-subscription setup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="ac43e-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="ac43e-140">Annak a helyi régiónak a felügyelt példányának a neve, amelyet fel szeretne venni a példány-feladatátvételi csoportba.</span><span class="sxs-lookup"><span data-stu-id="ac43e-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac43e-141">-ResourceGroupName</span></span>
<span data-ttu-id="ac43e-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac43e-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac43e-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac43e-143">-Confirm</span></span>
<span data-ttu-id="ac43e-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac43e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac43e-145">-WhatIf</span></span>
<span data-ttu-id="ac43e-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac43e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac43e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac43e-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac43e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac43e-148">CommonParameters</span></span>
<span data-ttu-id="ac43e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac43e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac43e-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac43e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac43e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac43e-151">INPUTS</span></span>

### <span data-ttu-id="ac43e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ac43e-152">System.String</span></span>

## <span data-ttu-id="ac43e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac43e-153">OUTPUTS</span></span>

### <span data-ttu-id="ac43e-154">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ac43e-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="ac43e-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac43e-155">NOTES</span></span>

## <span data-ttu-id="ac43e-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac43e-156">RELATED LINKS</span></span>
