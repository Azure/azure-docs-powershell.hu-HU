---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332921"
---
# <span data-ttu-id="82289-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82289-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="82289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82289-102">SYNOPSIS</span></span>
<span data-ttu-id="82289-103">Sql Data Warehouse-adatbázis felfüggesztése.</span><span class="sxs-lookup"><span data-stu-id="82289-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="82289-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82289-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82289-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82289-105">DESCRIPTION</span></span>
<span data-ttu-id="82289-106">A **Suspend-AzSqlDatabase** parancsmag felfüggeszti az Azure SQL Data Warehouse adatbázist.</span><span class="sxs-lookup"><span data-stu-id="82289-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="82289-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82289-107">EXAMPLES</span></span>

### <span data-ttu-id="82289-108">1. példa: Azure SQL Data Warehouse-adatbázis felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="82289-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="82289-109">Ez a parancs felfüggeszti egy aktív Azure SQL Data Warehouse-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="82289-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="82289-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82289-110">PARAMETERS</span></span>

### <span data-ttu-id="82289-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82289-111">-AsJob</span></span>
<span data-ttu-id="82289-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="82289-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82289-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82289-113">-DatabaseName</span></span>
<span data-ttu-id="82289-114">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="82289-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="82289-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82289-115">-DefaultProfile</span></span>
<span data-ttu-id="82289-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="82289-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82289-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82289-117">-ResourceGroupName</span></span>
<span data-ttu-id="82289-118">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="82289-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="82289-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="82289-119">-ServerName</span></span>
<span data-ttu-id="82289-120">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82289-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="82289-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82289-121">-Confirm</span></span>
<span data-ttu-id="82289-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82289-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82289-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82289-123">-WhatIf</span></span>
<span data-ttu-id="82289-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82289-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82289-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82289-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82289-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82289-126">CommonParameters</span></span>
<span data-ttu-id="82289-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82289-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82289-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82289-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82289-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82289-129">INPUTS</span></span>

### <span data-ttu-id="82289-130">System.String</span><span class="sxs-lookup"><span data-stu-id="82289-130">System.String</span></span>

## <span data-ttu-id="82289-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82289-131">OUTPUTS</span></span>

### <span data-ttu-id="82289-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="82289-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="82289-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82289-133">NOTES</span></span>
* <span data-ttu-id="82289-134">A **Suspend-AzSqlDatabase** parancsmag csak Azure SQL Data Warehouse-adatbázisokon működik.</span><span class="sxs-lookup"><span data-stu-id="82289-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="82289-135">Ez a művelet nem támogatott az Azure SQL Database Basic, Standard és Premium kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="82289-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="82289-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82289-136">RELATED LINKS</span></span>

[<span data-ttu-id="82289-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82289-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="82289-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82289-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="82289-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82289-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="82289-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82289-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="82289-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="82289-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="82289-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="82289-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


