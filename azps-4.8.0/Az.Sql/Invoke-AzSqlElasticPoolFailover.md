---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024370"
---
# <span data-ttu-id="c6da9-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="c6da9-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="c6da9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6da9-102">SYNOPSIS</span></span>
<span data-ttu-id="c6da9-103">A feladatátvételek rugalmas készletet mutatnak.</span><span class="sxs-lookup"><span data-stu-id="c6da9-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="c6da9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6da9-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6da9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6da9-105">DESCRIPTION</span></span>
<span data-ttu-id="c6da9-106">A Invoke-AzSqlElasticPoolFailover parancsmag rugalmas készletet hajt végre.</span><span class="sxs-lookup"><span data-stu-id="c6da9-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="c6da9-107">Az e parancsmag futtatását követően a rugalmas készlet minden adatbázisában feladatátvétel történik.</span><span class="sxs-lookup"><span data-stu-id="c6da9-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="c6da9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c6da9-108">EXAMPLES</span></span>

### <span data-ttu-id="c6da9-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6da9-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="c6da9-110">Ez a parancs a "Server01" nevű kiszolgálón a "ElasticPool01" nevű rugalmas készletet fogja átirányítani.</span><span class="sxs-lookup"><span data-stu-id="c6da9-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="c6da9-111">Ez azt jelenti, hogy a feladatátvétel a "ElasticPool01" nevű rugalmas készlet minden adatbázisában bekövetkezik.</span><span class="sxs-lookup"><span data-stu-id="c6da9-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="c6da9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6da9-112">PARAMETERS</span></span>

### <span data-ttu-id="c6da9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6da9-113">-AsJob</span></span>
<span data-ttu-id="c6da9-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c6da9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6da9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6da9-115">-DefaultProfile</span></span>
<span data-ttu-id="c6da9-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6da9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6da9-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c6da9-117">-ElasticPoolName</span></span>
<span data-ttu-id="c6da9-118">Annak az Azure SQL rugalmas készletnek a neve, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="c6da9-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="c6da9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c6da9-119">-Force</span></span>
<span data-ttu-id="c6da9-120">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="c6da9-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c6da9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6da9-121">-PassThru</span></span>
<span data-ttu-id="c6da9-122">Sikeres végrehajtás esetén az igaz értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c6da9-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="c6da9-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c6da9-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6da9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6da9-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6da9-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6da9-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6da9-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c6da9-126">-ServerName</span></span>
<span data-ttu-id="c6da9-127">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="c6da9-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="c6da9-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6da9-128">-Confirm</span></span>
<span data-ttu-id="c6da9-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6da9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6da9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6da9-130">-WhatIf</span></span>
<span data-ttu-id="c6da9-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6da9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6da9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6da9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6da9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6da9-133">CommonParameters</span></span>
<span data-ttu-id="c6da9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6da9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6da9-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6da9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6da9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6da9-136">INPUTS</span></span>

### <span data-ttu-id="c6da9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c6da9-137">System.String</span></span>

## <span data-ttu-id="c6da9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6da9-138">OUTPUTS</span></span>

## <span data-ttu-id="c6da9-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6da9-139">NOTES</span></span>

## <span data-ttu-id="c6da9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6da9-140">RELATED LINKS</span></span>

[<span data-ttu-id="c6da9-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6da9-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="c6da9-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c6da9-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="c6da9-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c6da9-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="c6da9-144">Meghívó-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="c6da9-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="c6da9-145">Új – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6da9-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="c6da9-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6da9-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="c6da9-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6da9-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="c6da9-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c6da9-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)