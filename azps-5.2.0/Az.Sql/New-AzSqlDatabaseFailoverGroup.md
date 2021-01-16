---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c1164f7c4875d6cdd00ca13236c1d8e6d4b07cb3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368982"
---
# <span data-ttu-id="422e5-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="422e5-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="422e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="422e5-102">SYNOPSIS</span></span>
<span data-ttu-id="422e5-103">Ez a parancs létrehoz egy új Azure SQL-adatbázis feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="422e5-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="422e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="422e5-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="422e5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="422e5-105">DESCRIPTION</span></span>
<span data-ttu-id="422e5-106">Létrehoz egy új Azure SQL-adatbázis feladatátvételi csoportot a megadott kiszolgálókhoz.</span><span class="sxs-lookup"><span data-stu-id="422e5-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="422e5-107">Két Azure SQL Database TDS-végpont jön létre a FailoverGroupName.SqlDatabaseDnsSuffix (például az FailoverGroupName.database.windows.net) és a FailoverGroupName.secondary.SqlDatabaseDnsSuffix fájlban.</span><span class="sxs-lookup"><span data-stu-id="422e5-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="422e5-108">Ezek a végpontok a feladatátvételi csoport elsődleges és másodlagos kiszolgálóihoz való csatlakozásra használhatók.</span><span class="sxs-lookup"><span data-stu-id="422e5-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="422e5-109">Ha az elsődleges kiszolgálót kimaradás érinti, a végpontok és adatbázisok automatikus feladatátvételét a feladatátvételi csoport feladatátvételi házirende és türelmi időszaka határozza meg.</span><span class="sxs-lookup"><span data-stu-id="422e5-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="422e5-110">Az újonnan létrehozott feladatátvételi csoportok nem tartalmaznak adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="422e5-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="422e5-111">A feladatátvételi csoportok adatbáziskészletének szabályozásához használja az "Add-AzSqlDatabaseToFailoverGroup" és a "Remove-AzSqlDatabaseFromFailoverGroup" parancsmagokat.</span><span class="sxs-lookup"><span data-stu-id="422e5-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="422e5-112">A "-GracePeriodWithDataLossHours" paraméter csak az 1 óránál nem kisebb értékeket támogatja.</span><span class="sxs-lookup"><span data-stu-id="422e5-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="422e5-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="422e5-113">EXAMPLES</span></span>

### <span data-ttu-id="422e5-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="422e5-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="422e5-115">Ez a parancs létrehoz egy új feladatátvételi csoportot, és az ugyanazon erőforráscsoport két kiszolgálója számára "Automatikus" feladatátvételi házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="422e5-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="422e5-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="422e5-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="422e5-117">Ez a parancs létrehoz egy új feladatátvételi csoportot, amely a "Kézi" feladatátvételi házirendet a különböző erőforráscsoportok két kiszolgálója számára hozza létre.</span><span class="sxs-lookup"><span data-stu-id="422e5-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="422e5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="422e5-118">PARAMETERS</span></span>

### <span data-ttu-id="422e5-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="422e5-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="422e5-120">A másodlagos kiszolgálón kimaradás esetén automatikus feladatátvételt kell-e kiváltanunk az írásra elérhető végponton.</span><span class="sxs-lookup"><span data-stu-id="422e5-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="422e5-121">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="422e5-121">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="422e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="422e5-122">-DefaultProfile</span></span>
<span data-ttu-id="422e5-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="422e5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="422e5-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="422e5-124">-FailoverGroupName</span></span>
<span data-ttu-id="422e5-125">A létrehozni szükséges Azure SQL-adatbázis feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="422e5-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="422e5-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="422e5-126">-FailoverPolicy</span></span>
<span data-ttu-id="422e5-127">Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételi házirende.</span><span class="sxs-lookup"><span data-stu-id="422e5-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="422e5-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="422e5-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="422e5-129">Az automatikus feladatátvétel indításakor eltelt időintervallum, ha kimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem fejezhető be adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="422e5-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="422e5-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="422e5-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="422e5-131">Az Azure SQL-adatbázis feladatátvételi csoportjának másodlagos erőforráscsoportja neve.</span><span class="sxs-lookup"><span data-stu-id="422e5-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="422e5-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="422e5-132">-PartnerServerName</span></span>
<span data-ttu-id="422e5-133">Az Azure SQL-adatbázis feladatátvételi csoportjának másodlagos kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="422e5-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="422e5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="422e5-134">-ResourceGroupName</span></span>
<span data-ttu-id="422e5-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="422e5-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="422e5-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="422e5-136">-ServerName</span></span>
<span data-ttu-id="422e5-137">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="422e5-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="422e5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="422e5-138">CommonParameters</span></span>
<span data-ttu-id="422e5-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="422e5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="422e5-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="422e5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="422e5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="422e5-141">INPUTS</span></span>

### <span data-ttu-id="422e5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="422e5-142">System.String</span></span>

## <span data-ttu-id="422e5-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="422e5-143">OUTPUTS</span></span>

### <span data-ttu-id="422e5-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="422e5-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="422e5-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="422e5-145">NOTES</span></span>

## <span data-ttu-id="422e5-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="422e5-146">RELATED LINKS</span></span>

[<span data-ttu-id="422e5-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="422e5-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="422e5-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="422e5-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="422e5-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="422e5-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="422e5-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="422e5-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="422e5-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="422e5-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="422e5-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="422e5-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="422e5-153">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="422e5-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
