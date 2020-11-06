---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492124"
---
# <span data-ttu-id="8fe60-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fe60-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="8fe60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fe60-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe60-103">A parancs létrehoz egy új Azure SQL-adatbázis feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="8fe60-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fe60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fe60-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fe60-105">DESCRIPTION</span></span>
<span data-ttu-id="8fe60-106">Új Azure SQL adatbázis-feladatátvételi csoportot hoz létre a megadott kiszolgálókhoz.</span><span class="sxs-lookup"><span data-stu-id="8fe60-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>

<span data-ttu-id="8fe60-107">Két Azure SQL-adatbázis TDS végpontokat hoz létre a FailoverGroupName. SqlDatabaseDnsSuffix (például FailoverGroupName.database.windows.net) és a FailoverGroupName. középfokú. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="8fe60-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="8fe60-108">Ezek a végpontok akkor használhatók, ha az elsődleges és a másodlagos kiszolgálókhoz csatlakoznak a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="8fe60-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="8fe60-109">Ha az elsődleges kiszolgálót áramkimaradás okozta, akkor a végpontok és adatbázisok automatikus feladatátvételét a feladatátvételi csoport feladatátvételi házirendje és türelmi időszaka határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8fe60-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="8fe60-110">Az újonnan létrehozott feladatátvevő csoportok nem tartalmaznak adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="8fe60-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="8fe60-111">Ha meg szeretné határozni egy feladatátvételi csoport adatbázis-készletét, használja a "AzureRmSqlDatabaseToFailoverGroup" és a "Remove-AzureRmSqlDatabaseFromFailoverGroup" parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8fe60-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>

<span data-ttu-id="8fe60-112">A feladatátvevő csoportok funkció előnézete során a "-GracePeriodWithDataLossHours" paraméterben csak az 1 óra feletti vagy azzal egyenlő értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="8fe60-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="8fe60-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8fe60-113">EXAMPLES</span></span>

### <span data-ttu-id="8fe60-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8fe60-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="8fe60-115">Ez a parancs létrehoz egy új feladatátvételi csoportot, amelyben az "automatikus" feladatátvételi házirend két kiszolgáló ugyanazon erőforráscsoport-kiszolgálón található.</span><span class="sxs-lookup"><span data-stu-id="8fe60-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="8fe60-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="8fe60-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="8fe60-117">Ez a parancs létrehoz egy új feladatátvételi csoportot, amelyben a feladatátvételi házirend "kézi", két különböző erőforráscsoport kiszolgálói esetén használható.</span><span class="sxs-lookup"><span data-stu-id="8fe60-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="8fe60-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fe60-118">PARAMETERS</span></span>

### <span data-ttu-id="8fe60-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="8fe60-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="8fe60-120">Azt, hogy a másodlagos kiszolgálón lévő leállás esetén az írásvédett végpont automatikus feladatátvételét kell-e elindítani.</span><span class="sxs-lookup"><span data-stu-id="8fe60-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="8fe60-121">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe60-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="8fe60-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe60-122">-DefaultProfile</span></span>
<span data-ttu-id="8fe60-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8fe60-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fe60-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe60-124">-FailoverGroupName</span></span>
<span data-ttu-id="8fe60-125">A létrehozandó Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fe60-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="8fe60-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe60-126">-FailoverPolicy</span></span>
<span data-ttu-id="8fe60-127">Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételi házirendje.</span><span class="sxs-lookup"><span data-stu-id="8fe60-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe60-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="8fe60-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="8fe60-129">Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem hajtható végre adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="8fe60-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe60-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe60-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="8fe60-131">Az Azure SQL-adatbázis feladatátvételi csoportjának másodlagos erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fe60-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="8fe60-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="8fe60-132">-PartnerServerName</span></span>
<span data-ttu-id="8fe60-133">Az Azure SQL-adatbázis feladatátvételi csoportjának másodlagos kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="8fe60-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="8fe60-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe60-134">-ResourceGroupName</span></span>
<span data-ttu-id="8fe60-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fe60-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe60-136">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8fe60-136">-ServerName</span></span>
<span data-ttu-id="8fe60-137">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="8fe60-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe60-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe60-138">CommonParameters</span></span>
<span data-ttu-id="8fe60-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fe60-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe60-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe60-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe60-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fe60-141">INPUTS</span></span>

### <span data-ttu-id="8fe60-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8fe60-142">System.String</span></span>

## <span data-ttu-id="8fe60-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fe60-143">OUTPUTS</span></span>

### <span data-ttu-id="8fe60-144">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="8fe60-144">System.Object</span></span>

## <span data-ttu-id="8fe60-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fe60-145">NOTES</span></span>

## <span data-ttu-id="8fe60-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fe60-146">RELATED LINKS</span></span>

[<span data-ttu-id="8fe60-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fe60-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8fe60-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fe60-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8fe60-149">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fe60-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="8fe60-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fe60-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="8fe60-151">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fe60-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8fe60-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fe60-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8fe60-153">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe60-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
