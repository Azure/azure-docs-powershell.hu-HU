---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/suspend-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: b4238ff85a35bcf6a48016a005af8a1f889332cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679653"
---
# <span data-ttu-id="f5455-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f5455-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f5455-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5455-102">SYNOPSIS</span></span>
<span data-ttu-id="f5455-103">Felfüggeszti az SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="f5455-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5455-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5455-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5455-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5455-105">DESCRIPTION</span></span>
<span data-ttu-id="f5455-106">A **felfüggesztés – AzureRmSqlDatabase** parancsmag felfüggeszti az Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="f5455-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="f5455-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f5455-107">EXAMPLES</span></span>

### <span data-ttu-id="f5455-108">1. példa: Azure SQL-adatraktár-adatbázis felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="f5455-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f5455-109">Ez a parancs felfüggeszti az aktív Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="f5455-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="f5455-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5455-110">PARAMETERS</span></span>

### <span data-ttu-id="f5455-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5455-111">-AsJob</span></span>
<span data-ttu-id="f5455-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f5455-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5455-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5455-113">-DatabaseName</span></span>
<span data-ttu-id="f5455-114">Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="f5455-114">Specifies the name of the database that this cmdlet suspends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5455-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5455-115">-DefaultProfile</span></span>
<span data-ttu-id="f5455-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f5455-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5455-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5455-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5455-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="f5455-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5455-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f5455-119">-ServerName</span></span>
<span data-ttu-id="f5455-120">Megadja az adatbázist tároló kiszolgáló nevét.</span><span class="sxs-lookup"><span data-stu-id="f5455-120">Specifies the name of the server which hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5455-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5455-121">-Confirm</span></span>
<span data-ttu-id="f5455-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5455-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5455-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5455-123">-WhatIf</span></span>
<span data-ttu-id="f5455-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5455-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5455-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5455-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5455-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5455-126">CommonParameters</span></span>
<span data-ttu-id="f5455-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5455-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5455-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5455-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5455-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5455-129">INPUTS</span></span>

### <span data-ttu-id="f5455-130">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f5455-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f5455-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5455-131">OUTPUTS</span></span>

### <span data-ttu-id="f5455-132">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f5455-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f5455-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5455-133">NOTES</span></span>
* <span data-ttu-id="f5455-134">A **felfüggesztés – AzureRmSqlDatabase** parancsmag csak az Azure SQL Data Warehouse-adatbázisokban működik.</span><span class="sxs-lookup"><span data-stu-id="f5455-134">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="f5455-135">Ez a művelet nem támogatott az Azure SQL-adatbázis Basic, standard és Premium kiadásaiban.</span><span class="sxs-lookup"><span data-stu-id="f5455-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="f5455-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5455-136">RELATED LINKS</span></span>

[<span data-ttu-id="f5455-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f5455-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f5455-138">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f5455-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f5455-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f5455-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f5455-140">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f5455-140">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f5455-141">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f5455-141">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="f5455-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5455-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


