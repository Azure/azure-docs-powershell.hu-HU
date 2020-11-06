---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: f2ee19834cdb4144c8f207ae8ff10a90a733bece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495639"
---
# <span data-ttu-id="712b5-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="712b5-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="712b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="712b5-102">SYNOPSIS</span></span>
<span data-ttu-id="712b5-103">Megkapja az adatbázist és a kibővített tulajdonság értékét.</span><span class="sxs-lookup"><span data-stu-id="712b5-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="712b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="712b5-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="712b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="712b5-105">DESCRIPTION</span></span>
<span data-ttu-id="712b5-106">A **Get-AzureRmSqlDatabaseExpanded** parancsmag az adatbázist és a kibővített tulajdonság értékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="712b5-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="712b5-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="712b5-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="712b5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="712b5-108">EXAMPLES</span></span>

### <span data-ttu-id="712b5-109">1. példa: az adatbázis-objektum beolvasása a Service Tier Advisor információkat tartalmazó adatokkal</span><span class="sxs-lookup"><span data-stu-id="712b5-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="712b5-110">Ez a parancs azt az adatbázist ad eredményül, amely a szolgáltatás Tier Advisor-információkat tartalmazó bővített tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="712b5-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="712b5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="712b5-111">PARAMETERS</span></span>

### <span data-ttu-id="712b5-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="712b5-112">-DatabaseName</span></span>
<span data-ttu-id="712b5-113">A beolvasott adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="712b5-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="712b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712b5-114">-DefaultProfile</span></span>
<span data-ttu-id="712b5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="712b5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="712b5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="712b5-116">-ResourceGroupName</span></span>
<span data-ttu-id="712b5-117">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="712b5-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="712b5-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="712b5-118">-ServerName</span></span>
<span data-ttu-id="712b5-119">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="712b5-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="712b5-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="712b5-120">-Confirm</span></span>
<span data-ttu-id="712b5-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="712b5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="712b5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="712b5-122">-WhatIf</span></span>
<span data-ttu-id="712b5-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="712b5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="712b5-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="712b5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="712b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712b5-125">CommonParameters</span></span>
<span data-ttu-id="712b5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="712b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712b5-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="712b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712b5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="712b5-128">INPUTS</span></span>

### <span data-ttu-id="712b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="712b5-129">System.String</span></span>

## <span data-ttu-id="712b5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="712b5-130">OUTPUTS</span></span>

### <span data-ttu-id="712b5-131">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="712b5-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="712b5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="712b5-132">NOTES</span></span>

## <span data-ttu-id="712b5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="712b5-133">RELATED LINKS</span></span>

[<span data-ttu-id="712b5-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="712b5-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
