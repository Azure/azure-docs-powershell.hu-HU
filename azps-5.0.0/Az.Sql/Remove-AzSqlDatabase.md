---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186648"
---
# <span data-ttu-id="d6273-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6273-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="d6273-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6273-102">SYNOPSIS</span></span>
<span data-ttu-id="d6273-103">Azure SQL-adatbázis eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d6273-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="d6273-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6273-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6273-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6273-105">DESCRIPTION</span></span>
<span data-ttu-id="d6273-106">A **Remove-AzSqlDatabase** parancsmag eltávolítja az Azure SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="d6273-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="d6273-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d6273-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d6273-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d6273-108">EXAMPLES</span></span>

### <span data-ttu-id="d6273-109">1. példa: adatbázis eltávolítása Azure SQL Server-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="d6273-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d6273-110">Ez a parancs eltávolítja a Database01 nevű adatbázist a kiszolgáló Server01.</span><span class="sxs-lookup"><span data-stu-id="d6273-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="d6273-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6273-111">PARAMETERS</span></span>

### <span data-ttu-id="d6273-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6273-112">-DatabaseName</span></span>
<span data-ttu-id="d6273-113">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d6273-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6273-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6273-114">-DefaultProfile</span></span>
<span data-ttu-id="d6273-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d6273-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6273-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d6273-116">-Force</span></span>
<span data-ttu-id="d6273-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d6273-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6273-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6273-118">-ResourceGroupName</span></span>
<span data-ttu-id="d6273-119">Annak az Azure erőforrás-csoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d6273-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d6273-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d6273-120">-ServerName</span></span>
<span data-ttu-id="d6273-121">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6273-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d6273-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6273-122">-Confirm</span></span>
<span data-ttu-id="d6273-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6273-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6273-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6273-124">-WhatIf</span></span>
<span data-ttu-id="d6273-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6273-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6273-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6273-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6273-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6273-127">CommonParameters</span></span>
<span data-ttu-id="d6273-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6273-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6273-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6273-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6273-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6273-130">INPUTS</span></span>

### <span data-ttu-id="d6273-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d6273-131">System.String</span></span>

## <span data-ttu-id="d6273-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6273-132">OUTPUTS</span></span>

### <span data-ttu-id="d6273-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d6273-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d6273-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6273-134">NOTES</span></span>

## <span data-ttu-id="d6273-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6273-135">RELATED LINKS</span></span>

[<span data-ttu-id="d6273-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6273-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="d6273-137">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6273-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="d6273-138">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6273-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="d6273-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6273-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="d6273-140">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6273-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="d6273-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d6273-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


