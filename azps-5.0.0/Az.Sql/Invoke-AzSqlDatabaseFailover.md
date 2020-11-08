---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185661"
---
# <span data-ttu-id="fe529-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="fe529-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="fe529-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe529-102">SYNOPSIS</span></span>
<span data-ttu-id="fe529-103">Egy adatbázis feladatátvétele</span><span class="sxs-lookup"><span data-stu-id="fe529-103">Failovers a database.</span></span>

## <span data-ttu-id="fe529-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe529-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe529-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe529-105">DESCRIPTION</span></span>
<span data-ttu-id="fe529-106">Az Invoke-AzSqlDatabaseFailover parancsmag az Azure SQL-adatbázist feladatátvételsel hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="fe529-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="fe529-107">Ha az adatbázis rugalmas készletben van, ez a parancs a megadott adatbázis feladatátvételét fogja biztosítani anélkül, hogy az ugyanazon rugalmas készlet többi adatbázisát befolyásolná.</span><span class="sxs-lookup"><span data-stu-id="fe529-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="fe529-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fe529-108">EXAMPLES</span></span>

### <span data-ttu-id="fe529-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fe529-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fe529-110">Ez a parancs a "Server01" nevű kiszolgálón az "Database01" nevű adatbázis elsődleges replikáját fogja lecserélni.</span><span class="sxs-lookup"><span data-stu-id="fe529-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="fe529-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="fe529-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="fe529-112">Ez a parancs a "Server01" nevű kiszolgálón a "Database01" nevű adatbázis olvasható másodlagos replikáját fogja átirányítani.</span><span class="sxs-lookup"><span data-stu-id="fe529-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="fe529-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe529-113">PARAMETERS</span></span>

### <span data-ttu-id="fe529-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe529-114">-AsJob</span></span>
<span data-ttu-id="fe529-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fe529-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe529-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe529-116">-DatabaseName</span></span>
<span data-ttu-id="fe529-117">A feladatátvételhez tartozó Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fe529-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="fe529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe529-118">-DefaultProfile</span></span>
<span data-ttu-id="fe529-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe529-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe529-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fe529-120">-Force</span></span>
<span data-ttu-id="fe529-121">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="fe529-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fe529-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe529-122">-PassThru</span></span>
<span data-ttu-id="fe529-123">Sikeres végrehajtás esetén az igaz értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="fe529-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="fe529-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fe529-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe529-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="fe529-125">-ReadableSecondary</span></span>
<span data-ttu-id="fe529-126">Az olvasható másodlagos replika feladatátvétele az alapértelmezett elsődleges replika helyett</span><span class="sxs-lookup"><span data-stu-id="fe529-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="fe529-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe529-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe529-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe529-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe529-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fe529-129">-ServerName</span></span>
<span data-ttu-id="fe529-130">Annak az Azure SQL adatbázis-kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="fe529-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="fe529-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe529-131">-Confirm</span></span>
<span data-ttu-id="fe529-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe529-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe529-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe529-133">-WhatIf</span></span>
<span data-ttu-id="fe529-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe529-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe529-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe529-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe529-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe529-136">CommonParameters</span></span>
<span data-ttu-id="fe529-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe529-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe529-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe529-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe529-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe529-139">INPUTS</span></span>

### <span data-ttu-id="fe529-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fe529-140">System.String</span></span>

## <span data-ttu-id="fe529-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe529-141">OUTPUTS</span></span>

## <span data-ttu-id="fe529-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe529-142">NOTES</span></span>

## <span data-ttu-id="fe529-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe529-143">RELATED LINKS</span></span>

[<span data-ttu-id="fe529-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe529-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="fe529-145">Meghívó-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="fe529-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="fe529-146">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe529-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="fe529-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe529-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="fe529-148">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe529-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="fe529-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe529-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="fe529-150">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe529-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="fe529-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe529-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)