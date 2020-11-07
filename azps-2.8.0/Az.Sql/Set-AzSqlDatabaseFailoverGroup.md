---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c354aa33ef4c86457d657e5c0197896669ce0b63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839293"
---
# <span data-ttu-id="f7cc8-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7cc8-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f7cc8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7cc8-103">Módosítja egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f7cc8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7cc8-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7cc8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="f7cc8-106">Ez a parancs módosítja egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="f7cc8-107">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="f7cc8-108">A csoportban lévő adatbázisok beállításához használja inkább az "Add-AzSqlDatabaseToFailoverGroup" és a "Remove-AzSqlDatabaseFromFailoverGroup" parancsot.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="f7cc8-109">A feladatátvevő csoportok funkció előnézete során a "-GracePeriodWithDataLossHours" paraméterben csak az 1 óra feletti vagy azzal egyenlő értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f7cc8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f7cc8-110">EXAMPLES</span></span>

### <span data-ttu-id="f7cc8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7cc8-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="f7cc8-112">A feladatátvételi csoport feladatátvételi házirendjét az "automatikus" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="f7cc8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f7cc8-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="f7cc8-114">A feladatátvételi csoport feladatátvételi házirendjét "kézi" értékre állítja a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="f7cc8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7cc8-115">PARAMETERS</span></span>

### <span data-ttu-id="f7cc8-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f7cc8-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f7cc8-117">Azt, hogy a másodlagos kiszolgálón hány kiesést kell kezdeményezni, a csak olvasható végpont automatikus feladatátvételét kell elindítania.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="f7cc8-118">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="f7cc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7cc8-119">-DefaultProfile</span></span>
<span data-ttu-id="f7cc8-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f7cc8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7cc8-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f7cc8-121">-FailoverGroupName</span></span>
<span data-ttu-id="f7cc8-122">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-122">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7cc8-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f7cc8-123">-FailoverPolicy</span></span>
<span data-ttu-id="f7cc8-124">Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételi házirendje.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f7cc8-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f7cc8-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f7cc8-126">Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="f7cc8-127">Ez azt jelzi, hogy az Azure SQL-adatbázis nem fog automatikus feladatátvételt kezdeményezni a türelmi időszak lejárta előtt.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="f7cc8-128">Felhívjuk a figyelmét arra, hogy a AllowDataLoss beállítással rendelkező feladatátvételi művelet az aszinkron szinkronizálás jellege miatt okozhatja az adatvesztést.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="f7cc8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7cc8-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7cc8-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="f7cc8-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f7cc8-131">-ServerName</span></span>
<span data-ttu-id="f7cc8-132">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f7cc8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7cc8-133">CommonParameters</span></span>
<span data-ttu-id="f7cc8-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7cc8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7cc8-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f7cc8-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7cc8-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7cc8-136">INPUTS</span></span>

### <span data-ttu-id="f7cc8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f7cc8-137">System.String</span></span>

## <span data-ttu-id="f7cc8-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7cc8-138">OUTPUTS</span></span>

### <span data-ttu-id="f7cc8-139">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f7cc8-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f7cc8-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7cc8-140">NOTES</span></span>

## <span data-ttu-id="f7cc8-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7cc8-141">RELATED LINKS</span></span>

[<span data-ttu-id="f7cc8-142">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7cc8-142">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f7cc8-143">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7cc8-143">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f7cc8-144">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7cc8-144">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f7cc8-145">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7cc8-145">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f7cc8-146">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7cc8-146">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f7cc8-147">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f7cc8-147">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f7cc8-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f7cc8-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
