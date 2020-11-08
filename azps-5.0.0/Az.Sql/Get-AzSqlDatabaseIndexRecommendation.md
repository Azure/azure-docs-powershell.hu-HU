---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185669"
---
# <span data-ttu-id="45907-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="45907-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="45907-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45907-102">SYNOPSIS</span></span>
<span data-ttu-id="45907-103">Az ajánlott indexelő műveleteket kapja meg egy kiszolgálón vagy adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="45907-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="45907-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45907-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45907-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45907-105">DESCRIPTION</span></span>
<span data-ttu-id="45907-106">A **Get-AzSqlDatabaseIndexRecommendation** parancsmag a javasolt indexelési műveleteket kapja meg egy Azure SQL-adatbázis kiszolgálója vagy adatbázisa számára.</span><span class="sxs-lookup"><span data-stu-id="45907-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="45907-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45907-107">EXAMPLES</span></span>

### <span data-ttu-id="45907-108">Példa 1: tárgymutató-javaslatok beszerzése minden adatbázisra a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="45907-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="45907-109">Ez a parancs a kiszolgálói server01 található összes adatbázis esetén a tárgymutatóra vonatkozó javaslatokat ad.</span><span class="sxs-lookup"><span data-stu-id="45907-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="45907-110">2. példa: egy adott adatbázis tárgymutató-ajánlásainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="45907-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="45907-111">Ez a parancs adott adatbázishoz tartozó tárgymutató-javaslatokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="45907-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="45907-112">3. példa: egyetlen tárgymutató-ajánlás beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="45907-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="45907-113">Ez a parancs név szerint ad eredményül egy tárgymutató-ajánlást.</span><span class="sxs-lookup"><span data-stu-id="45907-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="45907-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45907-114">PARAMETERS</span></span>

### <span data-ttu-id="45907-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45907-115">-DatabaseName</span></span>
<span data-ttu-id="45907-116">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja a tárgymutató-ajánlásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="45907-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45907-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45907-117">-DefaultProfile</span></span>
<span data-ttu-id="45907-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45907-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45907-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="45907-119">-IndexRecommendationName</span></span>
<span data-ttu-id="45907-120">Itt adhatja meg annak a tárgymutató-ajánlásnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="45907-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45907-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45907-121">-ResourceGroupName</span></span>
<span data-ttu-id="45907-122">Annak a csoportnak a neve, amelyhez a kiszolgáló van társítva.</span><span class="sxs-lookup"><span data-stu-id="45907-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="45907-123">Ez a parancsmag a kiszolgáló által üzemeltetett adatbázisok indexelési javaslatait kapja.</span><span class="sxs-lookup"><span data-stu-id="45907-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="45907-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="45907-124">-ServerName</span></span>
<span data-ttu-id="45907-125">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja az indexelési javaslatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="45907-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="45907-126">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="45907-126">-TableName</span></span>
<span data-ttu-id="45907-127">Egy Azure SQL-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45907-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45907-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45907-128">-Confirm</span></span>
<span data-ttu-id="45907-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45907-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45907-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45907-130">-WhatIf</span></span>
<span data-ttu-id="45907-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45907-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45907-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45907-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45907-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45907-133">CommonParameters</span></span>
<span data-ttu-id="45907-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45907-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45907-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45907-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45907-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45907-136">INPUTS</span></span>

### <span data-ttu-id="45907-137">System. String</span><span class="sxs-lookup"><span data-stu-id="45907-137">System.String</span></span>

## <span data-ttu-id="45907-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45907-138">OUTPUTS</span></span>

### <span data-ttu-id="45907-139">Microsoft. Azure. Command. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="45907-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="45907-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45907-140">NOTES</span></span>

## <span data-ttu-id="45907-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45907-141">RELATED LINKS</span></span>

[<span data-ttu-id="45907-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="45907-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="45907-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="45907-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
