---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193992"
---
# <span data-ttu-id="98537-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98537-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="98537-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98537-102">SYNOPSIS</span></span>
<span data-ttu-id="98537-103">Felfüggeszti az SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="98537-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="98537-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98537-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98537-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98537-105">DESCRIPTION</span></span>
<span data-ttu-id="98537-106">A **felfüggesztés – AzSqlDatabase** parancsmag felfüggeszti az Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="98537-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="98537-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98537-107">EXAMPLES</span></span>

### <span data-ttu-id="98537-108">1. példa: Azure SQL-adatraktár-adatbázis felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="98537-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="98537-109">Ez a parancs felfüggeszti az aktív Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="98537-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="98537-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98537-110">PARAMETERS</span></span>

### <span data-ttu-id="98537-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98537-111">-AsJob</span></span>
<span data-ttu-id="98537-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="98537-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98537-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="98537-113">-DatabaseName</span></span>
<span data-ttu-id="98537-114">Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="98537-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="98537-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98537-115">-DefaultProfile</span></span>
<span data-ttu-id="98537-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="98537-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98537-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98537-117">-ResourceGroupName</span></span>
<span data-ttu-id="98537-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="98537-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="98537-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="98537-119">-ServerName</span></span>
<span data-ttu-id="98537-120">Megadja az adatbázist tároló kiszolgáló nevét.</span><span class="sxs-lookup"><span data-stu-id="98537-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="98537-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98537-121">-Confirm</span></span>
<span data-ttu-id="98537-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98537-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98537-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98537-123">-WhatIf</span></span>
<span data-ttu-id="98537-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98537-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98537-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98537-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98537-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98537-126">CommonParameters</span></span>
<span data-ttu-id="98537-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98537-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98537-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="98537-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98537-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98537-129">INPUTS</span></span>

### <span data-ttu-id="98537-130">System. String</span><span class="sxs-lookup"><span data-stu-id="98537-130">System.String</span></span>

## <span data-ttu-id="98537-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98537-131">OUTPUTS</span></span>

### <span data-ttu-id="98537-132">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="98537-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="98537-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98537-133">NOTES</span></span>
* <span data-ttu-id="98537-134">A **felfüggesztés – AzSqlDatabase** parancsmag csak az Azure SQL Data Warehouse-adatbázisokban működik.</span><span class="sxs-lookup"><span data-stu-id="98537-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="98537-135">Ez a művelet nem támogatott az Azure SQL-adatbázis Basic, standard és Premium kiadásaiban.</span><span class="sxs-lookup"><span data-stu-id="98537-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="98537-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98537-136">RELATED LINKS</span></span>

[<span data-ttu-id="98537-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98537-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="98537-138">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98537-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="98537-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98537-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="98537-140">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98537-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="98537-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98537-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="98537-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="98537-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

