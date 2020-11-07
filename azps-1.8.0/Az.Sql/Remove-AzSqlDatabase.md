---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 200e53ef1f23c4b829380a2c8b7ca663443e5f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668864"
---
# <span data-ttu-id="41fc1-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41fc1-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="41fc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="41fc1-103">Azure SQL-adatbázis eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="41fc1-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="41fc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41fc1-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41fc1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="41fc1-106">A **Remove-AzSqlDatabase** parancsmag eltávolítja az Azure SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="41fc1-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="41fc1-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="41fc1-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="41fc1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="41fc1-108">EXAMPLES</span></span>

### <span data-ttu-id="41fc1-109">1. példa: adatbázis eltávolítása Azure SQL Server-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="41fc1-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="41fc1-110">Ez a parancs eltávolítja a Database01 nevű adatbázist a kiszolgáló Server01.</span><span class="sxs-lookup"><span data-stu-id="41fc1-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="41fc1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41fc1-111">PARAMETERS</span></span>

### <span data-ttu-id="41fc1-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41fc1-112">-DatabaseName</span></span>
<span data-ttu-id="41fc1-113">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="41fc1-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="41fc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fc1-114">-DefaultProfile</span></span>
<span data-ttu-id="41fc1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="41fc1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41fc1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="41fc1-116">-Force</span></span>
<span data-ttu-id="41fc1-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="41fc1-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41fc1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41fc1-118">-ResourceGroupName</span></span>
<span data-ttu-id="41fc1-119">Annak az Azure erőforrás-csoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="41fc1-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="41fc1-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="41fc1-120">-ServerName</span></span>
<span data-ttu-id="41fc1-121">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41fc1-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="41fc1-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41fc1-122">-Confirm</span></span>
<span data-ttu-id="41fc1-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41fc1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41fc1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41fc1-124">-WhatIf</span></span>
<span data-ttu-id="41fc1-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41fc1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41fc1-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41fc1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41fc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fc1-127">CommonParameters</span></span>
<span data-ttu-id="41fc1-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41fc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fc1-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41fc1-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fc1-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41fc1-130">INPUTS</span></span>

### <span data-ttu-id="41fc1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="41fc1-131">System.String</span></span>

## <span data-ttu-id="41fc1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41fc1-132">OUTPUTS</span></span>

### <span data-ttu-id="41fc1-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="41fc1-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="41fc1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41fc1-134">NOTES</span></span>

## <span data-ttu-id="41fc1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41fc1-135">RELATED LINKS</span></span>

[<span data-ttu-id="41fc1-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41fc1-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="41fc1-137">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41fc1-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="41fc1-138">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41fc1-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="41fc1-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41fc1-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="41fc1-140">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="41fc1-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="41fc1-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="41fc1-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


