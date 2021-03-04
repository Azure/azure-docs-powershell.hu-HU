---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 7b23bd6082fc79ff6096f496117c0ff6b63fd134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926354"
---
# <span data-ttu-id="26619-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="26619-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="26619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26619-102">SYNOPSIS</span></span>
<span data-ttu-id="26619-103">Az Azure SQL-adatbázis feladatátvételi csoportjainak levétele vagy listái.</span><span class="sxs-lookup"><span data-stu-id="26619-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="26619-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26619-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26619-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26619-105">DESCRIPTION</span></span>
<span data-ttu-id="26619-106">Egy adott Azure SQL-adatbázis feladatátvételi csoportot kap, vagy egy kiszolgálón felsorolja a feladatátvételi csoportokat.</span><span class="sxs-lookup"><span data-stu-id="26619-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="26619-107">A feladatátvételi csoport bármelyik kiszolgálója használható a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="26619-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="26619-108">A visszaadott értékek a megadott kiszolgáló állapotát tükrözik a feladatátvételi csoporttal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="26619-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="26619-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26619-109">EXAMPLES</span></span>

### <span data-ttu-id="26619-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="26619-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="26619-111">A kiszolgálón található összes feladatátvételi csoport listája.</span><span class="sxs-lookup"><span data-stu-id="26619-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="26619-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="26619-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="26619-113">Egy adott feladatátvételi csoport levétele.</span><span class="sxs-lookup"><span data-stu-id="26619-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="26619-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="26619-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="26619-115">Szerezze be az összes feladatátvételi csoportot egy olyan kiszolgálón, amely az "fg" kezdetsel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="26619-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="26619-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26619-116">PARAMETERS</span></span>

### <span data-ttu-id="26619-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26619-117">-DefaultProfile</span></span>
<span data-ttu-id="26619-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="26619-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26619-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="26619-119">-FailoverGroupName</span></span>
<span data-ttu-id="26619-120">A lekért Azure SQL-adatbázis feladatátvételi csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="26619-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="26619-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26619-121">-ResourceGroupName</span></span>
<span data-ttu-id="26619-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="26619-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="26619-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26619-123">-ServerName</span></span>
<span data-ttu-id="26619-124">Annak az Azure SQL Database Servernek a neve, amelyből lekéri a feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="26619-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="26619-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26619-125">CommonParameters</span></span>
<span data-ttu-id="26619-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26619-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26619-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26619-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26619-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26619-128">INPUTS</span></span>

### <span data-ttu-id="26619-129">System.String</span><span class="sxs-lookup"><span data-stu-id="26619-129">System.String</span></span>

## <span data-ttu-id="26619-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26619-130">OUTPUTS</span></span>

### <span data-ttu-id="26619-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="26619-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="26619-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26619-132">NOTES</span></span>

## <span data-ttu-id="26619-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26619-133">RELATED LINKS</span></span>

[<span data-ttu-id="26619-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="26619-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="26619-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="26619-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="26619-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="26619-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="26619-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="26619-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="26619-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="26619-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="26619-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="26619-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="26619-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="26619-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
