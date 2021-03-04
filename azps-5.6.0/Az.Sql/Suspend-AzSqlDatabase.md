---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 43284eb2f3d0cc39e5fcf5869ad26ebf0e52bd5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939346"
---
# <span data-ttu-id="bd140-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd140-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="bd140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd140-102">SYNOPSIS</span></span>
<span data-ttu-id="bd140-103">Sql Data Warehouse-adatbázis felfüggesztése.</span><span class="sxs-lookup"><span data-stu-id="bd140-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="bd140-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd140-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd140-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd140-105">DESCRIPTION</span></span>
<span data-ttu-id="bd140-106">A **Suspend-AzSqlDatabase** parancsmag felfüggeszti az Azure SQL Data Warehouse-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="bd140-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="bd140-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd140-107">EXAMPLES</span></span>

### <span data-ttu-id="bd140-108">1. példa: Azure SQL Data Warehouse-adatbázis felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="bd140-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="bd140-109">Ez a parancs felfüggeszti egy aktív Azure SQL Data Warehouse-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="bd140-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="bd140-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd140-110">PARAMETERS</span></span>

### <span data-ttu-id="bd140-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd140-111">-AsJob</span></span>
<span data-ttu-id="bd140-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bd140-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd140-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd140-113">-DatabaseName</span></span>
<span data-ttu-id="bd140-114">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="bd140-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="bd140-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd140-115">-DefaultProfile</span></span>
<span data-ttu-id="bd140-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bd140-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd140-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd140-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd140-118">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="bd140-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bd140-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd140-119">-ServerName</span></span>
<span data-ttu-id="bd140-120">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd140-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="bd140-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd140-121">-Confirm</span></span>
<span data-ttu-id="bd140-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd140-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd140-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd140-123">-WhatIf</span></span>
<span data-ttu-id="bd140-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd140-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd140-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd140-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd140-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd140-126">CommonParameters</span></span>
<span data-ttu-id="bd140-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd140-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd140-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd140-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd140-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd140-129">INPUTS</span></span>

### <span data-ttu-id="bd140-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bd140-130">System.String</span></span>

## <span data-ttu-id="bd140-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd140-131">OUTPUTS</span></span>

### <span data-ttu-id="bd140-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bd140-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bd140-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd140-133">NOTES</span></span>
* <span data-ttu-id="bd140-134">A **Suspend-AzSqlDatabase** parancsmag csak Azure SQL Data Warehouse-adatbázisokon működik.</span><span class="sxs-lookup"><span data-stu-id="bd140-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="bd140-135">Ez a művelet nem támogatott az Azure SQL Database Basic, Standard és Premium kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="bd140-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="bd140-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd140-136">RELATED LINKS</span></span>

[<span data-ttu-id="bd140-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd140-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="bd140-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd140-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="bd140-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd140-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="bd140-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd140-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="bd140-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd140-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="bd140-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bd140-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


