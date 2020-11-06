---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 1660c92ef4bef4cd832bc60506f7ef24d8927313
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505595"
---
# <span data-ttu-id="bdd90-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd90-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="bdd90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdd90-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd90-103">Azure SQL-adatbázis eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="bdd90-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdd90-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdd90-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdd90-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd90-106">A **Remove-AzureRmSqlDatabase** parancsmag eltávolítja az Azure SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="bdd90-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="bdd90-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bdd90-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bdd90-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bdd90-108">EXAMPLES</span></span>

### <span data-ttu-id="bdd90-109">1. példa: adatbázis eltávolítása Azure SQL Server-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="bdd90-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="bdd90-110">Ez a parancs eltávolítja a Database01 nevű adatbázist a kiszolgáló Server01.</span><span class="sxs-lookup"><span data-stu-id="bdd90-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="bdd90-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdd90-111">PARAMETERS</span></span>

### <span data-ttu-id="bdd90-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bdd90-112">-DatabaseName</span></span>
<span data-ttu-id="bdd90-113">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="bdd90-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bdd90-114">-Force</span><span class="sxs-lookup"><span data-stu-id="bdd90-114">-Force</span></span>
<span data-ttu-id="bdd90-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="bdd90-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bdd90-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd90-116">-ResourceGroupName</span></span>
<span data-ttu-id="bdd90-117">Annak az Azure erőforrás-csoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="bdd90-117">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="bdd90-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bdd90-118">-ServerName</span></span>
<span data-ttu-id="bdd90-119">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdd90-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="bdd90-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bdd90-120">-Confirm</span></span>
<span data-ttu-id="bdd90-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bdd90-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd90-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd90-122">-WhatIf</span></span>
<span data-ttu-id="bdd90-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bdd90-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd90-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdd90-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd90-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd90-125">-DefaultProfile</span></span>
<span data-ttu-id="bdd90-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdd90-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd90-127">CommonParameters</span></span>
<span data-ttu-id="bdd90-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdd90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd90-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd90-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd90-130">INPUTS</span></span>

### <span data-ttu-id="bdd90-131">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bdd90-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bdd90-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd90-132">OUTPUTS</span></span>

### <span data-ttu-id="bdd90-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bdd90-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bdd90-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdd90-134">NOTES</span></span>

## <span data-ttu-id="bdd90-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdd90-135">RELATED LINKS</span></span>

[<span data-ttu-id="bdd90-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd90-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="bdd90-137">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd90-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="bdd90-138">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd90-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="bdd90-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd90-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="bdd90-140">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd90-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="bdd90-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bdd90-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


