---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505572"
---
# <span data-ttu-id="a9c4b-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9c4b-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a9c4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c4b-103">Folytatja az SQL-adattárház-adatbázis lekérdezését.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9c4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9c4b-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c4b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c4b-106">A **resume-AzureRmSqlDatabase** parancsmag egy Azure SQL-adattárház adatbázist folytat.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a9c4b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a9c4b-107">EXAMPLES</span></span>

### <span data-ttu-id="a9c4b-108">1. példa: az Azure SQL Data Warehouse-adatbázis folytatása</span><span class="sxs-lookup"><span data-stu-id="a9c4b-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a9c4b-109">Ez a parancs folytatja a felfüggesztett Azure SQL-adattárház adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a9c4b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9c4b-110">PARAMETERS</span></span>

### <span data-ttu-id="a9c4b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9c4b-111">-DatabaseName</span></span>
<span data-ttu-id="a9c4b-112">Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag visszatér.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="a9c4b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c4b-113">-ResourceGroupName</span></span>
<span data-ttu-id="a9c4b-114">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a9c4b-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a9c4b-115">-ServerName</span></span>
<span data-ttu-id="a9c4b-116">Itt adhatja meg annak a kiszolgálónak a nevét, amely a parancsmag által folytatott adatbázist üzemelteti.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="a9c4b-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9c4b-117">-Confirm</span></span>
<span data-ttu-id="a9c4b-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c4b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c4b-119">-WhatIf</span></span>
<span data-ttu-id="a9c4b-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c4b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c4b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c4b-122">-DefaultProfile</span></span>
<span data-ttu-id="a9c4b-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9c4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c4b-124">CommonParameters</span></span>
<span data-ttu-id="a9c4b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9c4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c4b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c4b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c4b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9c4b-127">INPUTS</span></span>

### <span data-ttu-id="a9c4b-128">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a9c4b-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a9c4b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9c4b-129">OUTPUTS</span></span>

### <span data-ttu-id="a9c4b-130">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a9c4b-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a9c4b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9c4b-131">NOTES</span></span>
* <span data-ttu-id="a9c4b-132">A **resume-AzureRmSqlDatabase** parancsmag csak az Azure SQL Data Warehouse-adatbázisokban működik.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a9c4b-133">Ez a művelet nem támogatott az Azure SQL-adatbázis Basic, standard és Premium kiadásaiban.</span><span class="sxs-lookup"><span data-stu-id="a9c4b-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a9c4b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9c4b-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9c4b-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9c4b-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a9c4b-136">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9c4b-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="a9c4b-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9c4b-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a9c4b-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9c4b-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="a9c4b-139">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9c4b-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="a9c4b-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a9c4b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

