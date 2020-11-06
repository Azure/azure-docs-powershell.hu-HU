---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503155"
---
# <span data-ttu-id="bfb9f-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfb9f-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="bfb9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb9f-103">Felfüggeszti az SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfb9f-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfb9f-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb9f-106">A **felfüggesztés – AzureRmSqlDatabase** parancsmag felfüggeszti az Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="bfb9f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bfb9f-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb9f-108">1. példa: Azure SQL-adatraktár-adatbázis felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="bfb9f-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="bfb9f-109">Ez a parancs felfüggeszti az aktív Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="bfb9f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfb9f-110">PARAMETERS</span></span>

### <span data-ttu-id="bfb9f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bfb9f-111">-DatabaseName</span></span>
<span data-ttu-id="bfb9f-112">Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="bfb9f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb9f-113">-ResourceGroupName</span></span>
<span data-ttu-id="bfb9f-114">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bfb9f-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bfb9f-115">-ServerName</span></span>
<span data-ttu-id="bfb9f-116">Megadja az adatbázist tároló kiszolgáló nevét.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="bfb9f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bfb9f-117">-Confirm</span></span>
<span data-ttu-id="bfb9f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb9f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb9f-119">-WhatIf</span></span>
<span data-ttu-id="bfb9f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb9f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb9f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb9f-122">-DefaultProfile</span></span>
<span data-ttu-id="bfb9f-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb9f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb9f-124">CommonParameters</span></span>
<span data-ttu-id="bfb9f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfb9f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb9f-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb9f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb9f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfb9f-127">INPUTS</span></span>

### <span data-ttu-id="bfb9f-128">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bfb9f-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bfb9f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfb9f-129">OUTPUTS</span></span>

### <span data-ttu-id="bfb9f-130">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bfb9f-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bfb9f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfb9f-131">NOTES</span></span>
* <span data-ttu-id="bfb9f-132">A **felfüggesztés – AzureRmSqlDatabase** parancsmag csak az Azure SQL Data Warehouse-adatbázisokban működik.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="bfb9f-133">Ez a művelet nem támogatott az Azure SQL-adatbázis Basic, standard és Premium kiadásaiban.</span><span class="sxs-lookup"><span data-stu-id="bfb9f-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="bfb9f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfb9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="bfb9f-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfb9f-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="bfb9f-136">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfb9f-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="bfb9f-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfb9f-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="bfb9f-138">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfb9f-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="bfb9f-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfb9f-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="bfb9f-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bfb9f-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


