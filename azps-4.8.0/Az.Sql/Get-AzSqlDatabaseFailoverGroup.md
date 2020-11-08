---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024411"
---
# <span data-ttu-id="d5ded-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d5ded-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="d5ded-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5ded-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ded-103">Azure SQL adatbázis-feladatátvételi csoportok beolvasása vagy listázása.</span><span class="sxs-lookup"><span data-stu-id="d5ded-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="d5ded-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5ded-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5ded-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5ded-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ded-106">Egy bizonyos Azure SQL-adatbázis feladatátvételi csoportjának beolvasása vagy a feladatátvételi csoportok listázása a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="d5ded-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="d5ded-107">Előfordulhat, hogy a feladatátvételi csoport kiszolgálója használható a parancs végrehajtására.</span><span class="sxs-lookup"><span data-stu-id="d5ded-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="d5ded-108">A visszatérési értékek a megadott kiszolgáló állapotát tükrözik a feladatátvételi csoporttal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="d5ded-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="d5ded-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5ded-109">EXAMPLES</span></span>

### <span data-ttu-id="d5ded-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5ded-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="d5ded-111">A kiszolgálón lévő összes feladatátvételi csoport felsorolása.</span><span class="sxs-lookup"><span data-stu-id="d5ded-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="d5ded-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d5ded-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="d5ded-113">Adott feladatátvételi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5ded-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="d5ded-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="d5ded-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="d5ded-115">A "FG" kezdetű kiszolgáló minden feladatátvételi csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5ded-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="d5ded-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5ded-116">PARAMETERS</span></span>

### <span data-ttu-id="d5ded-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ded-117">-DefaultProfile</span></span>
<span data-ttu-id="d5ded-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d5ded-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5ded-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ded-119">-FailoverGroupName</span></span>
<span data-ttu-id="d5ded-120">A lekérdezni kívánt Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5ded-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ded-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ded-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5ded-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5ded-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5ded-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d5ded-123">-ServerName</span></span>
<span data-ttu-id="d5ded-124">Annak az Azure SQL adatbázis-kiszolgálónak a neve, amelyből a feladatátvételi csoportot be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="d5ded-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="d5ded-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ded-125">CommonParameters</span></span>
<span data-ttu-id="d5ded-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5ded-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ded-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d5ded-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ded-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5ded-128">INPUTS</span></span>

### <span data-ttu-id="d5ded-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d5ded-129">System.String</span></span>

## <span data-ttu-id="d5ded-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5ded-130">OUTPUTS</span></span>

### <span data-ttu-id="d5ded-131">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d5ded-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="d5ded-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5ded-132">NOTES</span></span>

## <span data-ttu-id="d5ded-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5ded-133">RELATED LINKS</span></span>

[<span data-ttu-id="d5ded-134">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d5ded-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d5ded-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d5ded-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d5ded-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d5ded-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="d5ded-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d5ded-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d5ded-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d5ded-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d5ded-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d5ded-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d5ded-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d5ded-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
