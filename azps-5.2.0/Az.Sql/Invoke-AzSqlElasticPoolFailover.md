---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364292"
---
# <span data-ttu-id="c6030-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="c6030-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="c6030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6030-102">SYNOPSIS</span></span>
<span data-ttu-id="c6030-103">Feladatátvétel egy rugalmas készletben.</span><span class="sxs-lookup"><span data-stu-id="c6030-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="c6030-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c6030-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6030-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c6030-105">DESCRIPTION</span></span>
<span data-ttu-id="c6030-106">A Invoke-AzSqlElasticPoolFailover parancsmag feladatátvétele egy rugalmas készletet.</span><span class="sxs-lookup"><span data-stu-id="c6030-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="c6030-107">A feladatátvétel a rugalmas készlet minden adatbázisában meg fog következni a parancsmag futtatása után.</span><span class="sxs-lookup"><span data-stu-id="c6030-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="c6030-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c6030-108">EXAMPLES</span></span>

### <span data-ttu-id="c6030-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c6030-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="c6030-110">Ez a parancs feladatátvételt ad a "Server01" nevű kiszolgálón található "RugalmasságPool01" nevű rugalmas készletnek.</span><span class="sxs-lookup"><span data-stu-id="c6030-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="c6030-111">Ez azt jelenti, hogy a feladatátvétel a RugalmasPool01 nevű rugalmas készlet minden adatbázisában meg fog következni.</span><span class="sxs-lookup"><span data-stu-id="c6030-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="c6030-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6030-112">PARAMETERS</span></span>

### <span data-ttu-id="c6030-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6030-113">-AsJob</span></span>
<span data-ttu-id="c6030-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c6030-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6030-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6030-115">-DefaultProfile</span></span>
<span data-ttu-id="c6030-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6030-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6030-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c6030-117">-ElasticPoolName</span></span>
<span data-ttu-id="c6030-118">Az eltávolítható Azure SQL-rugalmassági készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c6030-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="c6030-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c6030-119">-Force</span></span>
<span data-ttu-id="c6030-120">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="c6030-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c6030-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6030-121">-PassThru</span></span>
<span data-ttu-id="c6030-122">Sikeres végrehajtás esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c6030-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="c6030-123">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c6030-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6030-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6030-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6030-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6030-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6030-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6030-126">-ServerName</span></span>
<span data-ttu-id="c6030-127">Annak az Azure SQL Servernek a neve, amelynél a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="c6030-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="c6030-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6030-128">-Confirm</span></span>
<span data-ttu-id="c6030-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c6030-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6030-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6030-130">-WhatIf</span></span>
<span data-ttu-id="c6030-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c6030-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6030-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6030-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6030-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6030-133">CommonParameters</span></span>
<span data-ttu-id="c6030-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6030-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6030-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6030-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6030-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6030-136">INPUTS</span></span>

### <span data-ttu-id="c6030-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c6030-137">System.String</span></span>

## <span data-ttu-id="c6030-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6030-138">OUTPUTS</span></span>

## <span data-ttu-id="c6030-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c6030-139">NOTES</span></span>

## <span data-ttu-id="c6030-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6030-140">RELATED LINKS</span></span>

[<span data-ttu-id="c6030-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6030-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="c6030-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c6030-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="c6030-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c6030-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="c6030-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="c6030-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="c6030-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6030-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="c6030-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6030-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="c6030-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c6030-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="c6030-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c6030-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)