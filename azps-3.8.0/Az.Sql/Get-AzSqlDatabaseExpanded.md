---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011553"
---
# <span data-ttu-id="1c8b5-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="1c8b5-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="1c8b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8b5-103">Megkapja az adatbázist és a kibővített tulajdonság értékét.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="1c8b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c8b5-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c8b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="1c8b5-106">A **Get-AzSqlDatabaseExpanded** parancsmag az adatbázist és a kibővített tulajdonság értékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="1c8b5-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1c8b5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1c8b5-108">EXAMPLES</span></span>

### <span data-ttu-id="1c8b5-109">1. példa: az adatbázis-objektum beolvasása a Service Tier Advisor információkat tartalmazó adatokkal</span><span class="sxs-lookup"><span data-stu-id="1c8b5-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1c8b5-110">Ez a parancs azt az adatbázist ad eredményül, amely a szolgáltatás Tier Advisor-információkat tartalmazó bővített tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="1c8b5-111">2. példa: a lista adatbázis-objektumai szűréssel</span><span class="sxs-lookup"><span data-stu-id="1c8b5-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="1c8b5-112">Ez a parancs a kibontott adatbázis-objektumot a Server01-ban az "adatbázis" kezdetű adatbázisokban jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="1c8b5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c8b5-113">PARAMETERS</span></span>

### <span data-ttu-id="1c8b5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c8b5-114">-DatabaseName</span></span>
<span data-ttu-id="1c8b5-115">A beolvasott adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c8b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8b5-116">-DefaultProfile</span></span>
<span data-ttu-id="1c8b5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1c8b5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c8b5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c8b5-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c8b5-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1c8b5-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1c8b5-120">-ServerName</span></span>
<span data-ttu-id="1c8b5-121">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1c8b5-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1c8b5-122">-Confirm</span></span>
<span data-ttu-id="1c8b5-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c8b5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c8b5-124">-WhatIf</span></span>
<span data-ttu-id="1c8b5-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c8b5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c8b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8b5-127">CommonParameters</span></span>
<span data-ttu-id="1c8b5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c8b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8b5-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c8b5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8b5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c8b5-130">INPUTS</span></span>

### <span data-ttu-id="1c8b5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c8b5-131">System.String</span></span>

## <span data-ttu-id="1c8b5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c8b5-132">OUTPUTS</span></span>

### <span data-ttu-id="1c8b5-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="1c8b5-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="1c8b5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c8b5-134">NOTES</span></span>

## <span data-ttu-id="1c8b5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c8b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="1c8b5-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1c8b5-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
