---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 05f2de37ebeb477d45f96c415759ead3080a9e60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495524"
---
# <span data-ttu-id="25eb9-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="25eb9-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="25eb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="25eb9-103">Módosítja egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="25eb9-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25eb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25eb9-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25eb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="25eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="25eb9-106">Ez a parancs módosítja egy Azure SQL-adatbázis feladatátvételi csoportjának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="25eb9-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="25eb9-107">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="25eb9-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="25eb9-108">A csoportban lévő adatbázisok beállításához használja inkább az "Add-AzureRmSqlDatabaseToFailoverGroup" és a "Remove-AzureRmSqlDatabaseFromFailoverGroup" parancsot.</span><span class="sxs-lookup"><span data-stu-id="25eb9-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="25eb9-109">A feladatátvevő csoportok funkció előnézete során a "-GracePeriodWithDataLossHours" paraméterben csak az 1 óra feletti vagy azzal egyenlő értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="25eb9-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="25eb9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="25eb9-110">EXAMPLES</span></span>

### <span data-ttu-id="25eb9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25eb9-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="25eb9-112">A feladatátvételi csoport feladatátvételi házirendjét az "automatikus" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="25eb9-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="25eb9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="25eb9-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="25eb9-114">A feladatátvételi csoport feladatátvételi házirendjét "kézi" értékre állítja a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="25eb9-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="25eb9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25eb9-115">PARAMETERS</span></span>

### <span data-ttu-id="25eb9-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="25eb9-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="25eb9-117">Azt, hogy a másodlagos kiszolgálón hány kiesést kell kezdeményezni, a csak olvasható végpont automatikus feladatátvételét kell elindítania.</span><span class="sxs-lookup"><span data-stu-id="25eb9-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="25eb9-118">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="25eb9-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="25eb9-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="25eb9-119">-FailoverGroupName</span></span>
<span data-ttu-id="25eb9-120">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="25eb9-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="25eb9-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="25eb9-121">-FailoverPolicy</span></span>
<span data-ttu-id="25eb9-122">Az Azure SQL-adatbázis feladatátvételi csoportjának feladatátvételi házirendje.</span><span class="sxs-lookup"><span data-stu-id="25eb9-122">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="25eb9-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="25eb9-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="25eb9-124">Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem hajtható végre adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="25eb9-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="25eb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25eb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="25eb9-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="25eb9-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="25eb9-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="25eb9-127">-ServerName</span></span>
<span data-ttu-id="25eb9-128">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="25eb9-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="25eb9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25eb9-129">-DefaultProfile</span></span>
<span data-ttu-id="25eb9-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25eb9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25eb9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25eb9-131">CommonParameters</span></span>
<span data-ttu-id="25eb9-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25eb9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25eb9-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25eb9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25eb9-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25eb9-134">INPUTS</span></span>

### <span data-ttu-id="25eb9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="25eb9-135">System.String</span></span>

## <span data-ttu-id="25eb9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25eb9-136">OUTPUTS</span></span>

### <span data-ttu-id="25eb9-137">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="25eb9-137">System.Object</span></span>

## <span data-ttu-id="25eb9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25eb9-138">NOTES</span></span>

## <span data-ttu-id="25eb9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25eb9-139">RELATED LINKS</span></span>

[<span data-ttu-id="25eb9-140">Új – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="25eb9-140">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="25eb9-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="25eb9-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="25eb9-142">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="25eb9-142">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="25eb9-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="25eb9-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="25eb9-144">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="25eb9-144">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="25eb9-145">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="25eb9-145">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="25eb9-146">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="25eb9-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
