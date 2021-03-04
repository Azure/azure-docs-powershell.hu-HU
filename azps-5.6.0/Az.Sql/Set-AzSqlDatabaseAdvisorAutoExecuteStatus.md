---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 214fe4c32ed49433aa57752508604d0179334401
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940882"
---
# <span data-ttu-id="2db0a-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="2db0a-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="2db0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db0a-102">SYNOPSIS</span></span>
<span data-ttu-id="2db0a-103">Az Azure SQL-adatbázis tanácsadó automatikus végrehajtásának állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="2db0a-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="2db0a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2db0a-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db0a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2db0a-105">DESCRIPTION</span></span>
<span data-ttu-id="2db0a-106">A **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** parancsmag módosítja egy Azure SQL-adatbázis tanácsadó automatikus futtatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="2db0a-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="2db0a-107">Ez a parancsmag jelenleg az Engedélyezett, a Letiltott és az Alapértelmezett értékeket támogatja.</span><span class="sxs-lookup"><span data-stu-id="2db0a-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="2db0a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2db0a-108">EXAMPLES</span></span>

### <span data-ttu-id="2db0a-109">1. példa: Tanácsadó automatikus végrehajtásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2db0a-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="2db0a-110">Ez a parancs engedélyezi a CreateIndex nevű tanácsadó automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="2db0a-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="2db0a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2db0a-111">PARAMETERS</span></span>

### <span data-ttu-id="2db0a-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="2db0a-112">-AdvisorName</span></span>
<span data-ttu-id="2db0a-113">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja módosítja az állapotot.</span><span class="sxs-lookup"><span data-stu-id="2db0a-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db0a-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="2db0a-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="2db0a-115">Az állapot értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2db0a-115">Specifies the value for the status.</span></span>
<span data-ttu-id="2db0a-116">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="2db0a-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2db0a-117">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2db0a-117">Enabled</span></span> 
- <span data-ttu-id="2db0a-118">Letiltva</span><span class="sxs-lookup"><span data-stu-id="2db0a-118">Disabled</span></span> 
- <span data-ttu-id="2db0a-119">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="2db0a-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db0a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2db0a-120">-DatabaseName</span></span>
<span data-ttu-id="2db0a-121">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja módosítja az állapotát.</span><span class="sxs-lookup"><span data-stu-id="2db0a-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db0a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db0a-122">-DefaultProfile</span></span>
<span data-ttu-id="2db0a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2db0a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2db0a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db0a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2db0a-125">Az adatbázist tartalmazó kiszolgáló erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2db0a-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="2db0a-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2db0a-126">-ServerName</span></span>
<span data-ttu-id="2db0a-127">Az adatbázis kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2db0a-127">Specifies the name of the server for the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db0a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2db0a-128">-Confirm</span></span>
<span data-ttu-id="2db0a-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2db0a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db0a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db0a-130">-WhatIf</span></span>
<span data-ttu-id="2db0a-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2db0a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2db0a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2db0a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db0a-133">CommonParameters</span></span>
<span data-ttu-id="2db0a-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db0a-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2db0a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db0a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2db0a-136">INPUTS</span></span>

### <span data-ttu-id="2db0a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2db0a-137">System.String</span></span>

### <span data-ttu-id="2db0a-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="2db0a-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="2db0a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db0a-139">OUTPUTS</span></span>

### <span data-ttu-id="2db0a-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="2db0a-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="2db0a-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2db0a-141">NOTES</span></span>

## <span data-ttu-id="2db0a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2db0a-142">RELATED LINKS</span></span>

[<span data-ttu-id="2db0a-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="2db0a-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="2db0a-144">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2db0a-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

