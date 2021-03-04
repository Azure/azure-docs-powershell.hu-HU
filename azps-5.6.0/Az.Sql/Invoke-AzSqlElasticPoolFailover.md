---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 0af12c967dbbc65b37619ed837da1b8f778ab1db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931482"
---
# <span data-ttu-id="49f8b-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="49f8b-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="49f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="49f8b-103">Feladatátvétel egy rugalmas készletben.</span><span class="sxs-lookup"><span data-stu-id="49f8b-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="49f8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49f8b-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f8b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="49f8b-106">A Invoke-AzSqlElasticPoolFailover parancsmag feladatátvétele egy rugalmas készletet.</span><span class="sxs-lookup"><span data-stu-id="49f8b-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="49f8b-107">A feladatátvétel a rugalmas készlet minden adatbázisában meg fog következni a parancsmag futtatása után.</span><span class="sxs-lookup"><span data-stu-id="49f8b-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="49f8b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49f8b-108">EXAMPLES</span></span>

### <span data-ttu-id="49f8b-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="49f8b-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="49f8b-110">Ez a parancs feladatátvételt ad a "Server01" nevű kiszolgálón található "RugalmasságPool01" nevű rugalmas készletnek.</span><span class="sxs-lookup"><span data-stu-id="49f8b-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="49f8b-111">Ez azt jelenti, hogy a feladatátvétel a RugalmasPool01 nevű rugalmas készlet minden adatbázisában meg fog következni.</span><span class="sxs-lookup"><span data-stu-id="49f8b-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="49f8b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49f8b-112">PARAMETERS</span></span>

### <span data-ttu-id="49f8b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49f8b-113">-AsJob</span></span>
<span data-ttu-id="49f8b-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="49f8b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49f8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f8b-115">-DefaultProfile</span></span>
<span data-ttu-id="49f8b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49f8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f8b-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="49f8b-117">-ElasticPoolName</span></span>
<span data-ttu-id="49f8b-118">Az eltávolítható Azure SQL-rugalmassági készlet neve.</span><span class="sxs-lookup"><span data-stu-id="49f8b-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="49f8b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="49f8b-119">-Force</span></span>
<span data-ttu-id="49f8b-120">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="49f8b-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="49f8b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f8b-121">-PassThru</span></span>
<span data-ttu-id="49f8b-122">Sikeres végrehajtás esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="49f8b-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="49f8b-123">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="49f8b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49f8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="49f8b-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="49f8b-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="49f8b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49f8b-126">-ServerName</span></span>
<span data-ttu-id="49f8b-127">Annak az Azure SQL Servernek a neve, amelynél a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="49f8b-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="49f8b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49f8b-128">-Confirm</span></span>
<span data-ttu-id="49f8b-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49f8b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f8b-130">-WhatIf</span></span>
<span data-ttu-id="49f8b-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49f8b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49f8b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49f8b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f8b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f8b-133">CommonParameters</span></span>
<span data-ttu-id="49f8b-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f8b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f8b-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49f8b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f8b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49f8b-136">INPUTS</span></span>

### <span data-ttu-id="49f8b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="49f8b-137">System.String</span></span>

## <span data-ttu-id="49f8b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49f8b-138">OUTPUTS</span></span>

## <span data-ttu-id="49f8b-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49f8b-139">NOTES</span></span>

## <span data-ttu-id="49f8b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49f8b-140">RELATED LINKS</span></span>

[<span data-ttu-id="49f8b-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49f8b-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="49f8b-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="49f8b-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="49f8b-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="49f8b-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="49f8b-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="49f8b-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="49f8b-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49f8b-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="49f8b-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49f8b-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="49f8b-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49f8b-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="49f8b-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="49f8b-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)