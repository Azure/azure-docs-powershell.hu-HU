---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839431"
---
# <span data-ttu-id="7d38b-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="7d38b-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="7d38b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d38b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d38b-103">Egy adatbázis feladatátvétele</span><span class="sxs-lookup"><span data-stu-id="7d38b-103">Failovers a database.</span></span>

## <span data-ttu-id="7d38b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d38b-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d38b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d38b-105">DESCRIPTION</span></span>
<span data-ttu-id="7d38b-106">Az Invoke-AzSqlDatabaseFailover parancsmag az Azure SQL-adatbázist feladatátvételsel hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="7d38b-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="7d38b-107">Ha az adatbázis rugalmas készletben van, ez a parancs a megadott adatbázis feladatátvételét fogja biztosítani anélkül, hogy az ugyanazon rugalmas készlet többi adatbázisát befolyásolná.</span><span class="sxs-lookup"><span data-stu-id="7d38b-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="7d38b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7d38b-108">EXAMPLES</span></span>

### <span data-ttu-id="7d38b-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7d38b-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="7d38b-110">Ez a parancs a "Server01" nevű kiszolgálón az "Database01" nevű adatbázis feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="7d38b-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="7d38b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d38b-111">PARAMETERS</span></span>

### <span data-ttu-id="7d38b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d38b-112">-AsJob</span></span>
<span data-ttu-id="7d38b-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7d38b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d38b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d38b-114">-DatabaseName</span></span>
<span data-ttu-id="7d38b-115">A feladatátvételhez tartozó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7d38b-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="7d38b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d38b-116">-DefaultProfile</span></span>
<span data-ttu-id="7d38b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d38b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d38b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7d38b-118">-Force</span></span>
<span data-ttu-id="7d38b-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="7d38b-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7d38b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d38b-120">-PassThru</span></span>
<span data-ttu-id="7d38b-121">Sikeres végrehajtás esetén az igaz értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7d38b-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="7d38b-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7d38b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d38b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d38b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d38b-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7d38b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7d38b-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7d38b-125">-ServerName</span></span>
<span data-ttu-id="7d38b-126">Annak az Azure SQL adatbázis-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="7d38b-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="7d38b-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d38b-127">-Confirm</span></span>
<span data-ttu-id="7d38b-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d38b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d38b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d38b-129">-WhatIf</span></span>
<span data-ttu-id="7d38b-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d38b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d38b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d38b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d38b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d38b-132">CommonParameters</span></span>
<span data-ttu-id="7d38b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d38b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d38b-134">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d38b-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d38b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d38b-135">INPUTS</span></span>

### <span data-ttu-id="7d38b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7d38b-136">System.String</span></span>

## <span data-ttu-id="7d38b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d38b-137">OUTPUTS</span></span>

## <span data-ttu-id="7d38b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d38b-138">NOTES</span></span>

## <span data-ttu-id="7d38b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d38b-139">RELATED LINKS</span></span>

[<span data-ttu-id="7d38b-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7d38b-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="7d38b-141">Meghívó-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="7d38b-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="7d38b-142">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7d38b-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="7d38b-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7d38b-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="7d38b-144">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7d38b-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="7d38b-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7d38b-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="7d38b-146">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7d38b-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="7d38b-147">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7d38b-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
