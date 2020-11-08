---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181341"
---
# <span data-ttu-id="eed5c-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eed5c-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="eed5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eed5c-102">SYNOPSIS</span></span>
<span data-ttu-id="eed5c-103">Azure SQL-adatbázis eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="eed5c-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="eed5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eed5c-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eed5c-105">DESCRIPTION</span></span>
<span data-ttu-id="eed5c-106">A **Remove-AzSqlDatabase** parancsmag eltávolítja az Azure SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="eed5c-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="eed5c-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="eed5c-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="eed5c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="eed5c-108">EXAMPLES</span></span>

### <span data-ttu-id="eed5c-109">1. példa: adatbázis eltávolítása Azure SQL Server-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="eed5c-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="eed5c-110">Ez a parancs eltávolítja a Database01 nevű adatbázist a kiszolgáló Server01.</span><span class="sxs-lookup"><span data-stu-id="eed5c-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="eed5c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eed5c-111">PARAMETERS</span></span>

### <span data-ttu-id="eed5c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eed5c-112">-DatabaseName</span></span>
<span data-ttu-id="eed5c-113">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="eed5c-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eed5c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed5c-114">-DefaultProfile</span></span>
<span data-ttu-id="eed5c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="eed5c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eed5c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eed5c-116">-Force</span></span>
<span data-ttu-id="eed5c-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="eed5c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eed5c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed5c-118">-ResourceGroupName</span></span>
<span data-ttu-id="eed5c-119">Annak az Azure erőforrás-csoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="eed5c-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="eed5c-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="eed5c-120">-ServerName</span></span>
<span data-ttu-id="eed5c-121">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eed5c-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="eed5c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eed5c-122">-Confirm</span></span>
<span data-ttu-id="eed5c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eed5c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed5c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed5c-124">-WhatIf</span></span>
<span data-ttu-id="eed5c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eed5c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed5c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eed5c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed5c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed5c-127">CommonParameters</span></span>
<span data-ttu-id="eed5c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eed5c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed5c-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eed5c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed5c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eed5c-130">INPUTS</span></span>

### <span data-ttu-id="eed5c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="eed5c-131">System.String</span></span>

## <span data-ttu-id="eed5c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eed5c-132">OUTPUTS</span></span>

### <span data-ttu-id="eed5c-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eed5c-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="eed5c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eed5c-134">NOTES</span></span>

## <span data-ttu-id="eed5c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eed5c-135">RELATED LINKS</span></span>

[<span data-ttu-id="eed5c-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eed5c-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="eed5c-137">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eed5c-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="eed5c-138">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eed5c-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="eed5c-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eed5c-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="eed5c-140">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eed5c-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="eed5c-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="eed5c-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


