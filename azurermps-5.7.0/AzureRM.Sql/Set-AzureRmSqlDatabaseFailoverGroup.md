---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: e5452ef5b6d8b2e5535c5388d5d42698aa7c261f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494277"
---
# <span data-ttu-id="37687-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37687-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="37687-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37687-102">SYNOPSIS</span></span>
<span data-ttu-id="37687-103">Módosítja egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="37687-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37687-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37687-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37687-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37687-105">DESCRIPTION</span></span>
<span data-ttu-id="37687-106">Ez a parancs módosítja egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="37687-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="37687-107">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="37687-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="37687-108">A csoportban lévő adatbázisok beállításához használja inkább az "Add-AzureRmSqlDatabaseToFailoverGroup" és a "Remove-AzureRmSqlDatabaseFromFailoverGroup" parancsot.</span><span class="sxs-lookup"><span data-stu-id="37687-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="37687-109">A feladatátvevő csoportok funkció előnézete során a "-GracePeriodWithDataLossHours" paraméterben csak az 1 óra feletti vagy azzal egyenlő értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="37687-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="37687-110">Példák</span><span class="sxs-lookup"><span data-stu-id="37687-110">EXAMPLES</span></span>

### <span data-ttu-id="37687-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="37687-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="37687-112">A feladatátvételi csoport feladatátvételi házirendjét az "automatikus" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="37687-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="37687-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="37687-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="37687-114">A feladatátvételi csoport feladatátvételi házirendjét "kézi" értékre állítja a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="37687-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="37687-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37687-115">PARAMETERS</span></span>

### <span data-ttu-id="37687-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="37687-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="37687-117">Azt, hogy a másodlagos kiszolgálón hány kiesést kell kezdeményezni, a csak olvasható végpont automatikus feladatátvételét kell elindítania.</span><span class="sxs-lookup"><span data-stu-id="37687-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="37687-118">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="37687-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="37687-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37687-119">-DefaultProfile</span></span>
<span data-ttu-id="37687-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="37687-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37687-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="37687-121">-FailoverGroupName</span></span>
<span data-ttu-id="37687-122">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="37687-122">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37687-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="37687-123">-FailoverPolicy</span></span>
<span data-ttu-id="37687-124">Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételi házirendje.</span><span class="sxs-lookup"><span data-stu-id="37687-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="37687-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="37687-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="37687-126">Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="37687-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="37687-127">Ez azt jelzi, hogy az Azure SQL-adatbázis nem fog automatikus feladatátvételt kezdeményezni a türelmi időszak lejárta előtt.</span><span class="sxs-lookup"><span data-stu-id="37687-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="37687-128">Felhívjuk a figyelmét arra, hogy a AllowDataLoss beállítással rendelkező feladatátvételi művelet az aszinkron szinkronizálás jellege miatt okozhatja az adatvesztést.</span><span class="sxs-lookup"><span data-stu-id="37687-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="37687-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37687-129">-ResourceGroupName</span></span>
<span data-ttu-id="37687-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="37687-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="37687-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="37687-131">-ServerName</span></span>
<span data-ttu-id="37687-132">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="37687-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="37687-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37687-133">CommonParameters</span></span>
<span data-ttu-id="37687-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37687-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37687-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37687-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37687-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37687-136">INPUTS</span></span>

### <span data-ttu-id="37687-137">System. String</span><span class="sxs-lookup"><span data-stu-id="37687-137">System.String</span></span>

## <span data-ttu-id="37687-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37687-138">OUTPUTS</span></span>

### <span data-ttu-id="37687-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="37687-139">System.Object</span></span>

## <span data-ttu-id="37687-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37687-140">NOTES</span></span>

## <span data-ttu-id="37687-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37687-141">RELATED LINKS</span></span>

[<span data-ttu-id="37687-142">Új – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37687-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="37687-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37687-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="37687-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37687-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="37687-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37687-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="37687-146">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37687-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="37687-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37687-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="37687-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="37687-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
