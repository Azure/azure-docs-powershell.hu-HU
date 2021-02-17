---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207878"
---
# <span data-ttu-id="1319e-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1319e-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="1319e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1319e-102">SYNOPSIS</span></span>
<span data-ttu-id="1319e-103">Egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="1319e-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="1319e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1319e-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1319e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1319e-105">DESCRIPTION</span></span>
<span data-ttu-id="1319e-106">Ez a parancs módosítja egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1319e-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="1319e-107">A feladatátvételi csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="1319e-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="1319e-108">A csoportban szereplő adatbázisok szabályozásához használja az "Add-AzSqlDatabaseToFailoverGroup" és a "Remove-AzSqlDatabaseFromFailoverGroup" ehelyett.</span><span class="sxs-lookup"><span data-stu-id="1319e-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="1319e-109">A Feladatátvételi csoportok funkció előzetes verziója csak az 1 óránál nem kisebb értékeket támogatja a "-GracePeriodWithDataLossHours" paraméterben.</span><span class="sxs-lookup"><span data-stu-id="1319e-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="1319e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1319e-110">EXAMPLES</span></span>

### <span data-ttu-id="1319e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1319e-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="1319e-112">A feladatátvételi csoport feladatátvételi házirendet automatikusra állítja.</span><span class="sxs-lookup"><span data-stu-id="1319e-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="1319e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1319e-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="1319e-114">A feladatátvételi csoport feladatátvételi házirendjének "Kézi" beállítását állítja be a feladatátvételi csoportban.</span><span class="sxs-lookup"><span data-stu-id="1319e-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="1319e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1319e-115">PARAMETERS</span></span>

### <span data-ttu-id="1319e-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="1319e-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="1319e-117">A másodlagos kiszolgálón a kimaradás az írásra csak olvasható végpont automatikus feladatátvételét váltja-e ki.</span><span class="sxs-lookup"><span data-stu-id="1319e-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="1319e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1319e-118">-DefaultProfile</span></span>
<span data-ttu-id="1319e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1319e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1319e-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="1319e-120">-FailoverGroupName</span></span>
<span data-ttu-id="1319e-121">Az Azure SQL-adatbázis feladatátvételi csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="1319e-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="1319e-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1319e-122">-FailoverPolicy</span></span>
<span data-ttu-id="1319e-123">Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételi házirende.</span><span class="sxs-lookup"><span data-stu-id="1319e-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="1319e-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="1319e-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="1319e-125">Az automatikus feladatátvétel indításakor eltelt időintervallum, ha kimaradás történik az elsődleges kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="1319e-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="1319e-126">Ez azt jelenti, hogy az Azure SQL-adatbázis nem kezdeményez automatikus feladatátvételt a türelmi időszak lejárta előtt.</span><span class="sxs-lookup"><span data-stu-id="1319e-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="1319e-127">Felhívjuk a figyelmét arra, hogy az AllowDataLoss beállítás feladatátvételi művelete adatvesztést okozhat az aszinkron szinkronizálás természete miatt.</span><span class="sxs-lookup"><span data-stu-id="1319e-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="1319e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1319e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1319e-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1319e-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="1319e-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1319e-130">-ServerName</span></span>
<span data-ttu-id="1319e-131">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="1319e-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="1319e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1319e-132">CommonParameters</span></span>
<span data-ttu-id="1319e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1319e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1319e-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1319e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1319e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1319e-135">INPUTS</span></span>

### <span data-ttu-id="1319e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1319e-136">System.String</span></span>

## <span data-ttu-id="1319e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1319e-137">OUTPUTS</span></span>

### <span data-ttu-id="1319e-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1319e-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="1319e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1319e-139">NOTES</span></span>

## <span data-ttu-id="1319e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1319e-140">RELATED LINKS</span></span>

[<span data-ttu-id="1319e-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1319e-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1319e-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1319e-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1319e-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1319e-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="1319e-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1319e-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="1319e-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1319e-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1319e-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1319e-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1319e-147">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1319e-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
