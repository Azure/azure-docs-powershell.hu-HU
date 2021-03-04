---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 2a4142c7d8bb0f48bf75613b214dccd1876c5264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921593"
---
# <span data-ttu-id="403b7-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="403b7-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="403b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="403b7-102">SYNOPSIS</span></span>
<span data-ttu-id="403b7-103">Eltávolít egy Azure SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="403b7-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="403b7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="403b7-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="403b7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="403b7-105">DESCRIPTION</span></span>
<span data-ttu-id="403b7-106">A **Remove-AzSqlDatabase** parancsmag eltávolít egy Azure SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="403b7-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="403b7-107">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="403b7-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="403b7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="403b7-108">EXAMPLES</span></span>

### <span data-ttu-id="403b7-109">1. példa: Adatbázis eltávolítása Azure SQL-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="403b7-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="403b7-110">Ez a parancs eltávolítja az Adatbázis01 nevű adatbázist a kiszolgáló Kiszolgáló01 kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="403b7-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="403b7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="403b7-111">PARAMETERS</span></span>

### <span data-ttu-id="403b7-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="403b7-112">-DatabaseName</span></span>
<span data-ttu-id="403b7-113">Annak az adatbázisnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="403b7-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="403b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403b7-114">-DefaultProfile</span></span>
<span data-ttu-id="403b7-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="403b7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="403b7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="403b7-116">-Force</span></span>
<span data-ttu-id="403b7-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="403b7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="403b7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="403b7-118">-ResourceGroupName</span></span>
<span data-ttu-id="403b7-119">Annak az Azure-erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="403b7-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="403b7-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="403b7-120">-ServerName</span></span>
<span data-ttu-id="403b7-121">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="403b7-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="403b7-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="403b7-122">-Confirm</span></span>
<span data-ttu-id="403b7-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="403b7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="403b7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="403b7-124">-WhatIf</span></span>
<span data-ttu-id="403b7-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="403b7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="403b7-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="403b7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="403b7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403b7-127">CommonParameters</span></span>
<span data-ttu-id="403b7-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="403b7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403b7-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="403b7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403b7-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="403b7-130">INPUTS</span></span>

### <span data-ttu-id="403b7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="403b7-131">System.String</span></span>

## <span data-ttu-id="403b7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="403b7-132">OUTPUTS</span></span>

### <span data-ttu-id="403b7-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="403b7-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="403b7-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="403b7-134">NOTES</span></span>

## <span data-ttu-id="403b7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="403b7-135">RELATED LINKS</span></span>

[<span data-ttu-id="403b7-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="403b7-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="403b7-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="403b7-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="403b7-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="403b7-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="403b7-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="403b7-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="403b7-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="403b7-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="403b7-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="403b7-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


