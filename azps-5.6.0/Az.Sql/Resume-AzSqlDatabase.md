---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: 3ba3703882371975ee9b0d2f87bd03b75b58e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940897"
---
# <span data-ttu-id="843d0-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="843d0-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="843d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="843d0-102">SYNOPSIS</span></span>
<span data-ttu-id="843d0-103">Sql Data Warehouse-adatbázis folytatása.</span><span class="sxs-lookup"><span data-stu-id="843d0-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="843d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="843d0-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="843d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="843d0-105">DESCRIPTION</span></span>
<span data-ttu-id="843d0-106">A **Resume-AzSqlDatabase** parancsmag egy Azure SQL Data Warehouse-adatbázist folytat.</span><span class="sxs-lookup"><span data-stu-id="843d0-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="843d0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="843d0-107">EXAMPLES</span></span>

### <span data-ttu-id="843d0-108">1. példa: Azure SQL Data Warehouse-adatbázis folytatása</span><span class="sxs-lookup"><span data-stu-id="843d0-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="843d0-109">Ez a parancs egy felfüggesztett Azure SQL Data Warehouse-adatbázist folytat.</span><span class="sxs-lookup"><span data-stu-id="843d0-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="843d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="843d0-110">PARAMETERS</span></span>

### <span data-ttu-id="843d0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="843d0-111">-AsJob</span></span>
<span data-ttu-id="843d0-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="843d0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="843d0-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="843d0-113">-DatabaseName</span></span>
<span data-ttu-id="843d0-114">Annak az adatbázisnak a nevét adja meg, amelyről a parancsmag folytatódik.</span><span class="sxs-lookup"><span data-stu-id="843d0-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="843d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="843d0-115">-DefaultProfile</span></span>
<span data-ttu-id="843d0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="843d0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="843d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="843d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="843d0-118">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="843d0-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="843d0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="843d0-119">-ServerName</span></span>
<span data-ttu-id="843d0-120">Annak a kiszolgálónak a nevét adja meg, amely a parancsmag által folytatható adatbázist tárolja.</span><span class="sxs-lookup"><span data-stu-id="843d0-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="843d0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="843d0-121">-Confirm</span></span>
<span data-ttu-id="843d0-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="843d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="843d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="843d0-123">-WhatIf</span></span>
<span data-ttu-id="843d0-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="843d0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="843d0-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="843d0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="843d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843d0-126">CommonParameters</span></span>
<span data-ttu-id="843d0-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="843d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843d0-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="843d0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843d0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="843d0-129">INPUTS</span></span>

### <span data-ttu-id="843d0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="843d0-130">System.String</span></span>

## <span data-ttu-id="843d0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="843d0-131">OUTPUTS</span></span>

### <span data-ttu-id="843d0-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="843d0-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="843d0-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="843d0-133">NOTES</span></span>
* <span data-ttu-id="843d0-134">A **Resume-AzSqlDatabase** parancsmag csak Azure SQL Data Warehouse-adatbázisokon működik.</span><span class="sxs-lookup"><span data-stu-id="843d0-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="843d0-135">Ez a művelet nem támogatott az Azure SQL Database Basic, Standard és Premium kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="843d0-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="843d0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="843d0-136">RELATED LINKS</span></span>

[<span data-ttu-id="843d0-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="843d0-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="843d0-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="843d0-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="843d0-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="843d0-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="843d0-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="843d0-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="843d0-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="843d0-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="843d0-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="843d0-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


