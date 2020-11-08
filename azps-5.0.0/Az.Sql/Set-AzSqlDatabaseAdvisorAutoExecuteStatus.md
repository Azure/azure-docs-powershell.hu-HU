---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194513"
---
# <span data-ttu-id="aa227-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="aa227-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="aa227-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa227-102">SYNOPSIS</span></span>
<span data-ttu-id="aa227-103">Egy Azure SQL-adatbázis-tanácsadó automatikus végrehajtási állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="aa227-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="aa227-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa227-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa227-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa227-105">DESCRIPTION</span></span>
<span data-ttu-id="aa227-106">A **set-AzSqlDatabaseAdvisorAutoExecuteStatus** parancsmag módosította az Azure SQL-adatbázis-tanácsadók automatikus végrehajtás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="aa227-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="aa227-107">Ez a parancsmag jelenleg az engedélyezett, a letiltott és az alapértelmezett értéket támogatja.</span><span class="sxs-lookup"><span data-stu-id="aa227-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="aa227-108">Példák</span><span class="sxs-lookup"><span data-stu-id="aa227-108">EXAMPLES</span></span>

### <span data-ttu-id="aa227-109">1. példa: az automatikus végrehajtás engedélyezése egy tanácsadónál</span><span class="sxs-lookup"><span data-stu-id="aa227-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="aa227-110">Ez a parancs módosítja egy CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="aa227-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="aa227-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa227-111">PARAMETERS</span></span>

### <span data-ttu-id="aa227-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="aa227-112">-AdvisorName</span></span>
<span data-ttu-id="aa227-113">Annak a tanácsadónak a nevét adja meg, amelyhez ez a parancsmag módosította az állapotot.</span><span class="sxs-lookup"><span data-stu-id="aa227-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="aa227-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="aa227-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="aa227-115">Az állapot értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa227-115">Specifies the value for the status.</span></span>
<span data-ttu-id="aa227-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aa227-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa227-117">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="aa227-117">Enabled</span></span> 
- <span data-ttu-id="aa227-118">Tiltva</span><span class="sxs-lookup"><span data-stu-id="aa227-118">Disabled</span></span> 
- <span data-ttu-id="aa227-119">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="aa227-119">Default</span></span>

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

### <span data-ttu-id="aa227-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa227-120">-DatabaseName</span></span>
<span data-ttu-id="aa227-121">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja módosította az állapotot.</span><span class="sxs-lookup"><span data-stu-id="aa227-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="aa227-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa227-122">-DefaultProfile</span></span>
<span data-ttu-id="aa227-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aa227-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa227-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa227-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa227-125">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa227-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="aa227-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="aa227-126">-ServerName</span></span>
<span data-ttu-id="aa227-127">Az adatbázis kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa227-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="aa227-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa227-128">-Confirm</span></span>
<span data-ttu-id="aa227-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa227-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa227-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa227-130">-WhatIf</span></span>
<span data-ttu-id="aa227-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa227-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa227-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa227-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa227-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa227-133">CommonParameters</span></span>
<span data-ttu-id="aa227-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa227-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa227-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa227-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa227-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa227-136">INPUTS</span></span>

### <span data-ttu-id="aa227-137">System. String</span><span class="sxs-lookup"><span data-stu-id="aa227-137">System.String</span></span>

### <span data-ttu-id="aa227-138">Microsoft. Azure. Command. SQL. Advisor. parancsmag. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="aa227-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="aa227-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa227-139">OUTPUTS</span></span>

### <span data-ttu-id="aa227-140">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="aa227-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="aa227-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa227-141">NOTES</span></span>

## <span data-ttu-id="aa227-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa227-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa227-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="aa227-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="aa227-144">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa227-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

