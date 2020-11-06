---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: e2d263bdf7e7011a97183e464ee967415c281715
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498175"
---
# <span data-ttu-id="8fee4-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8fee4-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="8fee4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fee4-102">SYNOPSIS</span></span>
<span data-ttu-id="8fee4-103">Azure SQL-adatbázis eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8fee4-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fee4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fee4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fee4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fee4-105">DESCRIPTION</span></span>
<span data-ttu-id="8fee4-106">A **Remove-AzureRmSqlDatabase** parancsmag eltávolítja az Azure SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="8fee4-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="8fee4-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="8fee4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8fee4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8fee4-108">EXAMPLES</span></span>

### <span data-ttu-id="8fee4-109">1. példa: adatbázis eltávolítása Azure SQL Server-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="8fee4-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8fee4-110">Ez a parancs eltávolítja a Database01 nevű adatbázist a kiszolgáló Server01.</span><span class="sxs-lookup"><span data-stu-id="8fee4-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="8fee4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fee4-111">PARAMETERS</span></span>

### <span data-ttu-id="8fee4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8fee4-112">-DatabaseName</span></span>
<span data-ttu-id="8fee4-113">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="8fee4-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8fee4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fee4-114">-DefaultProfile</span></span>
<span data-ttu-id="8fee4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8fee4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fee4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8fee4-116">-Force</span></span>
<span data-ttu-id="8fee4-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8fee4-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fee4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fee4-118">-ResourceGroupName</span></span>
<span data-ttu-id="8fee4-119">Annak az Azure erőforrás-csoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8fee4-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8fee4-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8fee4-120">-ServerName</span></span>
<span data-ttu-id="8fee4-121">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fee4-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8fee4-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8fee4-122">-Confirm</span></span>
<span data-ttu-id="8fee4-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8fee4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fee4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fee4-124">-WhatIf</span></span>
<span data-ttu-id="8fee4-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8fee4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fee4-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fee4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fee4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fee4-127">CommonParameters</span></span>
<span data-ttu-id="8fee4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fee4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fee4-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fee4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fee4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fee4-130">INPUTS</span></span>

### <span data-ttu-id="8fee4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8fee4-131">System.String</span></span>

## <span data-ttu-id="8fee4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fee4-132">OUTPUTS</span></span>

### <span data-ttu-id="8fee4-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8fee4-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8fee4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fee4-134">NOTES</span></span>

## <span data-ttu-id="8fee4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fee4-135">RELATED LINKS</span></span>

[<span data-ttu-id="8fee4-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8fee4-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="8fee4-137">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8fee4-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="8fee4-138">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8fee4-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="8fee4-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8fee4-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="8fee4-140">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8fee4-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="8fee4-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fee4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


