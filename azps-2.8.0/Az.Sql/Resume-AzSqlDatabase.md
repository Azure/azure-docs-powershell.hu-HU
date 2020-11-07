---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: c5f30388e1e3cb804aa0ef8d45e0afe34a1d2cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839091"
---
# <span data-ttu-id="c2236-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c2236-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="c2236-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2236-102">SYNOPSIS</span></span>
<span data-ttu-id="c2236-103">Folytatja az SQL-adattárház-adatbázis lekérdezését.</span><span class="sxs-lookup"><span data-stu-id="c2236-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="c2236-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2236-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2236-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2236-105">DESCRIPTION</span></span>
<span data-ttu-id="c2236-106">A **resume-AzSqlDatabase** parancsmag egy Azure SQL-adattárház adatbázist folytat.</span><span class="sxs-lookup"><span data-stu-id="c2236-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="c2236-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c2236-107">EXAMPLES</span></span>

### <span data-ttu-id="c2236-108">1. példa: az Azure SQL Data Warehouse-adatbázis folytatása</span><span class="sxs-lookup"><span data-stu-id="c2236-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c2236-109">Ez a parancs folytatja a felfüggesztett Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="c2236-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="c2236-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2236-110">PARAMETERS</span></span>

### <span data-ttu-id="c2236-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2236-111">-AsJob</span></span>
<span data-ttu-id="c2236-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c2236-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2236-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2236-113">-DatabaseName</span></span>
<span data-ttu-id="c2236-114">Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag visszatér.</span><span class="sxs-lookup"><span data-stu-id="c2236-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="c2236-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2236-115">-DefaultProfile</span></span>
<span data-ttu-id="c2236-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c2236-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2236-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2236-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2236-118">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c2236-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c2236-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c2236-119">-ServerName</span></span>
<span data-ttu-id="c2236-120">Itt adhatja meg annak a kiszolgálónak a nevét, amely a parancsmag által folytatott adatbázist üzemelteti.</span><span class="sxs-lookup"><span data-stu-id="c2236-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="c2236-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2236-121">-Confirm</span></span>
<span data-ttu-id="c2236-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2236-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2236-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2236-123">-WhatIf</span></span>
<span data-ttu-id="c2236-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c2236-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2236-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2236-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2236-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2236-126">CommonParameters</span></span>
<span data-ttu-id="c2236-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2236-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2236-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c2236-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2236-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2236-129">INPUTS</span></span>

### <span data-ttu-id="c2236-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c2236-130">System.String</span></span>

## <span data-ttu-id="c2236-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2236-131">OUTPUTS</span></span>

### <span data-ttu-id="c2236-132">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c2236-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c2236-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2236-133">NOTES</span></span>
* <span data-ttu-id="c2236-134">A **resume-AzSqlDatabase** parancsmag csak az Azure SQL Data Warehouse-adatbázisokban működik.</span><span class="sxs-lookup"><span data-stu-id="c2236-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="c2236-135">Ez a művelet nem támogatott az Azure SQL-adatbázis Basic, standard és Premium kiadásaiban.</span><span class="sxs-lookup"><span data-stu-id="c2236-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="c2236-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2236-136">RELATED LINKS</span></span>

[<span data-ttu-id="c2236-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c2236-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="c2236-138">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c2236-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="c2236-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c2236-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="c2236-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c2236-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="c2236-141">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c2236-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="c2236-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c2236-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


