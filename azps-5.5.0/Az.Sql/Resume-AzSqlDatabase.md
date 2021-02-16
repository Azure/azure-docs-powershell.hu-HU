---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168642"
---
# <span data-ttu-id="b32a6-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b32a6-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="b32a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b32a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b32a6-103">Sql Data Warehouse-adatbázis folytatása.</span><span class="sxs-lookup"><span data-stu-id="b32a6-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="b32a6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b32a6-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32a6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b32a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b32a6-106">A **Resume-AzSqlDatabase** parancsmag egy Azure SQL Data Warehouse-adatbázist folytat.</span><span class="sxs-lookup"><span data-stu-id="b32a6-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="b32a6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b32a6-107">EXAMPLES</span></span>

### <span data-ttu-id="b32a6-108">1. példa: Azure SQL Data Warehouse-adatbázis folytatása</span><span class="sxs-lookup"><span data-stu-id="b32a6-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b32a6-109">Ez a parancs egy felfüggesztett Azure SQL Data Warehouse-adatbázist folytat.</span><span class="sxs-lookup"><span data-stu-id="b32a6-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="b32a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b32a6-110">PARAMETERS</span></span>

### <span data-ttu-id="b32a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b32a6-111">-AsJob</span></span>
<span data-ttu-id="b32a6-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b32a6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b32a6-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b32a6-113">-DatabaseName</span></span>
<span data-ttu-id="b32a6-114">Annak az adatbázisnak a nevét adja meg, amelyről a parancsmag folytatódik.</span><span class="sxs-lookup"><span data-stu-id="b32a6-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="b32a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32a6-115">-DefaultProfile</span></span>
<span data-ttu-id="b32a6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b32a6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b32a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="b32a6-118">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b32a6-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b32a6-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b32a6-119">-ServerName</span></span>
<span data-ttu-id="b32a6-120">Annak a kiszolgálónak a nevét adja meg, amely a parancsmag által folytatható adatbázist tárolja.</span><span class="sxs-lookup"><span data-stu-id="b32a6-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="b32a6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b32a6-121">-Confirm</span></span>
<span data-ttu-id="b32a6-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b32a6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32a6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32a6-123">-WhatIf</span></span>
<span data-ttu-id="b32a6-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b32a6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b32a6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b32a6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32a6-126">CommonParameters</span></span>
<span data-ttu-id="b32a6-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b32a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32a6-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b32a6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32a6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b32a6-129">INPUTS</span></span>

### <span data-ttu-id="b32a6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b32a6-130">System.String</span></span>

## <span data-ttu-id="b32a6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32a6-131">OUTPUTS</span></span>

### <span data-ttu-id="b32a6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b32a6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b32a6-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b32a6-133">NOTES</span></span>
* <span data-ttu-id="b32a6-134">A **Resume-AzSqlDatabase** parancsmag csak Azure SQL Data Warehouse-adatbázisokon működik.</span><span class="sxs-lookup"><span data-stu-id="b32a6-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="b32a6-135">Ez a művelet nem támogatott az Azure SQL Database Basic, a Standard és a Premium kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="b32a6-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="b32a6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b32a6-136">RELATED LINKS</span></span>

[<span data-ttu-id="b32a6-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b32a6-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b32a6-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b32a6-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="b32a6-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b32a6-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="b32a6-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b32a6-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="b32a6-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b32a6-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="b32a6-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b32a6-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


