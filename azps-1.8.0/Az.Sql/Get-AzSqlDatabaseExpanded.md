---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 9ff2284e602fe0bb9a7afea886385a02f89298a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669038"
---
# <span data-ttu-id="7deb6-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="7deb6-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="7deb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7deb6-102">SYNOPSIS</span></span>
<span data-ttu-id="7deb6-103">Megkapja az adatbázist és a kibővített tulajdonság értékét.</span><span class="sxs-lookup"><span data-stu-id="7deb6-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="7deb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7deb6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7deb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7deb6-105">DESCRIPTION</span></span>
<span data-ttu-id="7deb6-106">A **Get-AzSqlDatabaseExpanded** parancsmag az adatbázist és a kibővített tulajdonság értékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7deb6-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="7deb6-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="7deb6-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7deb6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7deb6-108">EXAMPLES</span></span>

### <span data-ttu-id="7deb6-109">1. példa: az adatbázis-objektum beolvasása a Service Tier Advisor információkat tartalmazó adatokkal</span><span class="sxs-lookup"><span data-stu-id="7deb6-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="7deb6-110">Ez a parancs azt az adatbázist ad eredményül, amely a szolgáltatás Tier Advisor-információkat tartalmazó bővített tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7deb6-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="7deb6-111">2. példa: a lista adatbázis-objektumai szűréssel</span><span class="sxs-lookup"><span data-stu-id="7deb6-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="7deb6-112">Ez a parancs a kibontott adatbázis-objektumot a Server01-ban az "adatbázis" kezdetű adatbázisokban jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7deb6-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="7deb6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7deb6-113">PARAMETERS</span></span>

### <span data-ttu-id="7deb6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7deb6-114">-DatabaseName</span></span>
<span data-ttu-id="7deb6-115">A beolvasott adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7deb6-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7deb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7deb6-116">-DefaultProfile</span></span>
<span data-ttu-id="7deb6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7deb6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7deb6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7deb6-118">-ResourceGroupName</span></span>
<span data-ttu-id="7deb6-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="7deb6-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7deb6-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7deb6-120">-ServerName</span></span>
<span data-ttu-id="7deb6-121">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7deb6-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7deb6-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7deb6-122">-Confirm</span></span>
<span data-ttu-id="7deb6-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7deb6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7deb6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7deb6-124">-WhatIf</span></span>
<span data-ttu-id="7deb6-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7deb6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7deb6-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7deb6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7deb6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7deb6-127">CommonParameters</span></span>
<span data-ttu-id="7deb6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7deb6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7deb6-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7deb6-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7deb6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7deb6-130">INPUTS</span></span>

### <span data-ttu-id="7deb6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7deb6-131">System.String</span></span>

## <span data-ttu-id="7deb6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7deb6-132">OUTPUTS</span></span>

### <span data-ttu-id="7deb6-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="7deb6-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="7deb6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7deb6-134">NOTES</span></span>

## <span data-ttu-id="7deb6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7deb6-135">RELATED LINKS</span></span>

[<span data-ttu-id="7deb6-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7deb6-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
