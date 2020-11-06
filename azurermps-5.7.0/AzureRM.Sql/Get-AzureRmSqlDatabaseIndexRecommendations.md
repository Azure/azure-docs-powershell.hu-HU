---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseindexrecommendations
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: 6e9622565017f71c8b73e70e7aa4d0c3528bc254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492143"
---
# <span data-ttu-id="21798-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="21798-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="21798-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21798-102">SYNOPSIS</span></span>
<span data-ttu-id="21798-103">Az ajánlott indexelő műveleteket kapja meg egy kiszolgálón vagy adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="21798-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21798-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21798-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21798-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21798-105">DESCRIPTION</span></span>
<span data-ttu-id="21798-106">A **Get-AzureRmSqlDatabaseIndexRecommendations** parancsmag a javasolt indexelési műveleteket kapja meg egy Azure SQL-adatbázis kiszolgálója vagy adatbázisa számára.</span><span class="sxs-lookup"><span data-stu-id="21798-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="21798-107">Példák</span><span class="sxs-lookup"><span data-stu-id="21798-107">EXAMPLES</span></span>

### <span data-ttu-id="21798-108">Példa 1: tárgymutató-javaslatok beszerzése minden adatbázisra a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="21798-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="21798-109">Ez a parancs a kiszolgálói server01 található összes adatbázis esetén a tárgymutatóra vonatkozó javaslatokat ad.</span><span class="sxs-lookup"><span data-stu-id="21798-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="21798-110">2. példa: egy adott adatbázis tárgymutató-ajánlásainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="21798-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="21798-111">Ez a parancs adott adatbázishoz tartozó tárgymutató-javaslatokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="21798-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="21798-112">3. példa: egyetlen tárgymutató-ajánlás beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="21798-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="21798-113">Ez a parancs név szerint ad eredményül egy tárgymutató-ajánlást.</span><span class="sxs-lookup"><span data-stu-id="21798-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="21798-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21798-114">PARAMETERS</span></span>

### <span data-ttu-id="21798-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21798-115">-DatabaseName</span></span>
<span data-ttu-id="21798-116">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja a tárgymutató-ajánlásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="21798-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21798-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21798-117">-DefaultProfile</span></span>
<span data-ttu-id="21798-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="21798-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21798-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="21798-119">-IndexRecommendationName</span></span>
<span data-ttu-id="21798-120">Itt adhatja meg annak a tárgymutató-ajánlásnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="21798-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21798-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21798-121">-ResourceGroupName</span></span>
<span data-ttu-id="21798-122">Annak a csoportnak a neve, amelyhez a kiszolgáló van társítva.</span><span class="sxs-lookup"><span data-stu-id="21798-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="21798-123">Ez a parancsmag a kiszolgáló által üzemeltetett adatbázisok indexelési javaslatait kapja.</span><span class="sxs-lookup"><span data-stu-id="21798-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="21798-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="21798-124">-ServerName</span></span>
<span data-ttu-id="21798-125">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja az indexelési javaslatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="21798-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="21798-126">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="21798-126">-TableName</span></span>
<span data-ttu-id="21798-127">Egy Azure SQL-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21798-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21798-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21798-128">-Confirm</span></span>
<span data-ttu-id="21798-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21798-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21798-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21798-130">-WhatIf</span></span>
<span data-ttu-id="21798-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21798-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21798-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21798-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21798-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21798-133">CommonParameters</span></span>
<span data-ttu-id="21798-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21798-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21798-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21798-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21798-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21798-136">INPUTS</span></span>

### <span data-ttu-id="21798-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="21798-137">None</span></span>
<span data-ttu-id="21798-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="21798-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21798-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21798-139">OUTPUTS</span></span>

## <span data-ttu-id="21798-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21798-140">NOTES</span></span>

## <span data-ttu-id="21798-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21798-141">RELATED LINKS</span></span>

[<span data-ttu-id="21798-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="21798-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="21798-143">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="21798-143">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)
