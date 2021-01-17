---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375030"
---
# <span data-ttu-id="cccbf-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cccbf-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="cccbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccbf-102">SYNOPSIS</span></span>
<span data-ttu-id="cccbf-103">Az Azure SQL-adatbázis feladatátvételi csoportjainak levétele vagy listái.</span><span class="sxs-lookup"><span data-stu-id="cccbf-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="cccbf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cccbf-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cccbf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cccbf-105">DESCRIPTION</span></span>
<span data-ttu-id="cccbf-106">Egy adott Azure SQL-adatbázis feladatátvételi csoportot kap, vagy egy kiszolgálón felsorolja a feladatátvételi csoportokat.</span><span class="sxs-lookup"><span data-stu-id="cccbf-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="cccbf-107">A feladatátvételi csoport bármelyik kiszolgálója használható a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="cccbf-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="cccbf-108">A visszaadott értékek a megadott kiszolgáló állapotát tükrözik a feladatátvételi csoporttal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="cccbf-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="cccbf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cccbf-109">EXAMPLES</span></span>

### <span data-ttu-id="cccbf-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cccbf-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="cccbf-111">A kiszolgálón található összes feladatátvételi csoport listája.</span><span class="sxs-lookup"><span data-stu-id="cccbf-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="cccbf-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cccbf-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="cccbf-113">Adott feladatátvételi csoport levétele.</span><span class="sxs-lookup"><span data-stu-id="cccbf-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="cccbf-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="cccbf-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="cccbf-115">Szerezze be az összes feladatátvételi csoportot egy olyan kiszolgálón, amely az "fg" kezdetekkel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="cccbf-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="cccbf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cccbf-116">PARAMETERS</span></span>

### <span data-ttu-id="cccbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccbf-117">-DefaultProfile</span></span>
<span data-ttu-id="cccbf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cccbf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cccbf-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="cccbf-119">-FailoverGroupName</span></span>
<span data-ttu-id="cccbf-120">A lekért Azure SQL-adatbázis feladatátvételi csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="cccbf-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="cccbf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cccbf-121">-ResourceGroupName</span></span>
<span data-ttu-id="cccbf-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cccbf-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="cccbf-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cccbf-123">-ServerName</span></span>
<span data-ttu-id="cccbf-124">Annak az Azure SQL Database Servernek a neve, amelyből lekéri a feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="cccbf-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="cccbf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccbf-125">CommonParameters</span></span>
<span data-ttu-id="cccbf-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccbf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccbf-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cccbf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccbf-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cccbf-128">INPUTS</span></span>

### <span data-ttu-id="cccbf-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cccbf-129">System.String</span></span>

## <span data-ttu-id="cccbf-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cccbf-130">OUTPUTS</span></span>

### <span data-ttu-id="cccbf-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="cccbf-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="cccbf-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cccbf-132">NOTES</span></span>

## <span data-ttu-id="cccbf-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cccbf-133">RELATED LINKS</span></span>

[<span data-ttu-id="cccbf-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cccbf-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cccbf-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cccbf-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cccbf-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cccbf-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="cccbf-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cccbf-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="cccbf-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cccbf-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cccbf-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cccbf-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cccbf-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="cccbf-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
