---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374679"
---
# <span data-ttu-id="6e783-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="6e783-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="6e783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e783-102">SYNOPSIS</span></span>
<span data-ttu-id="6e783-103">Egy adatbázis feladatátvétele.</span><span class="sxs-lookup"><span data-stu-id="6e783-103">Failovers a database.</span></span>

## <span data-ttu-id="6e783-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e783-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e783-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e783-105">DESCRIPTION</span></span>
<span data-ttu-id="6e783-106">A Invoke-AzSqlDatabaseFailover parancsmag feladatátvétele egy Azure SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="6e783-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="6e783-107">Ha az adatbázis rugalmas készletben van, ez a parancs feladatátvételt ad az adott adatbázisnak anélkül, hogy hatással lenne az ugyanabban a rugalmas készletben található többi adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="6e783-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="6e783-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e783-108">EXAMPLES</span></span>

### <span data-ttu-id="6e783-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="6e783-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="6e783-110">Ez a parancs feladatátvételt ad a "Server01" nevű kiszolgálón található "Database01" nevű adatbázis elsődleges másolatának.</span><span class="sxs-lookup"><span data-stu-id="6e783-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="6e783-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="6e783-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="6e783-112">Ez a parancs feladatátvételt ad a "Server01" nevű kiszolgálón található "Database01" nevű adatbázis olvasható másodlagos másolatának.</span><span class="sxs-lookup"><span data-stu-id="6e783-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="6e783-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e783-113">PARAMETERS</span></span>

### <span data-ttu-id="6e783-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e783-114">-AsJob</span></span>
<span data-ttu-id="6e783-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6e783-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e783-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e783-116">-DatabaseName</span></span>
<span data-ttu-id="6e783-117">A feladatátvételre megfelelő Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6e783-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e783-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e783-118">-DefaultProfile</span></span>
<span data-ttu-id="6e783-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e783-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e783-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6e783-120">-Force</span></span>
<span data-ttu-id="6e783-121">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="6e783-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e783-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e783-122">-PassThru</span></span>
<span data-ttu-id="6e783-123">Sikeres végrehajtás esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="6e783-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="6e783-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6e783-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e783-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="6e783-125">-ReadableSecondary</span></span>
<span data-ttu-id="6e783-126">Az alapértelmezett elsődleges replika helyett az olvasható másodlagos replika feladatátvétele</span><span class="sxs-lookup"><span data-stu-id="6e783-126">Failover the readable secondary replica instead of the default primary replica</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e783-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e783-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e783-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6e783-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e783-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e783-129">-ServerName</span></span>
<span data-ttu-id="6e783-130">Annak az Azure SQL Database Servernek a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="6e783-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="6e783-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e783-131">-Confirm</span></span>
<span data-ttu-id="6e783-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e783-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e783-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e783-133">-WhatIf</span></span>
<span data-ttu-id="6e783-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e783-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e783-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e783-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e783-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e783-136">CommonParameters</span></span>
<span data-ttu-id="6e783-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e783-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e783-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e783-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e783-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e783-139">INPUTS</span></span>

### <span data-ttu-id="6e783-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6e783-140">System.String</span></span>

## <span data-ttu-id="6e783-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e783-141">OUTPUTS</span></span>

## <span data-ttu-id="6e783-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e783-142">NOTES</span></span>

## <span data-ttu-id="6e783-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e783-143">RELATED LINKS</span></span>

[<span data-ttu-id="6e783-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e783-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="6e783-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="6e783-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="6e783-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e783-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="6e783-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e783-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="6e783-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e783-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="6e783-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e783-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="6e783-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e783-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="6e783-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6e783-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
