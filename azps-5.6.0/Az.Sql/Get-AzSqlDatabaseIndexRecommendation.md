---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 2205c241625f0bfdc2be21cda34c5bc3d6d07c12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014806"
---
# <span data-ttu-id="75418-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="75418-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="75418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75418-102">SYNOPSIS</span></span>
<span data-ttu-id="75418-103">A kiszolgálóhoz vagy adatbázishoz ajánlott indexműveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="75418-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="75418-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75418-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75418-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75418-105">DESCRIPTION</span></span>
<span data-ttu-id="75418-106">A **Get-AzSqlDatabaseIndexRecommendation** parancsmag megkapja az Ajánlott indexműveleteket egy Azure SQL-adatbázis-kiszolgálóhoz vagy -adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="75418-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="75418-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75418-107">EXAMPLES</span></span>

### <span data-ttu-id="75418-108">1. példa: Index-javaslatok lekérte a kiszolgálón található összes adatbázist</span><span class="sxs-lookup"><span data-stu-id="75418-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="75418-109">Ez a parancs a kiszolgálókiszolgáló01 kiszolgálón található összes adatbázisra vonatkozó indexjavaslatokat ad vissza.</span><span class="sxs-lookup"><span data-stu-id="75418-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="75418-110">2. példa: Index-javaslatok lekérte egy adott adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="75418-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="75418-111">Ez a parancs adott adatbázis index-javaslatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="75418-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="75418-112">3. példa: Egyetlen ajánlott index létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="75418-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="75418-113">Ez a parancs név szerint egy index ajánlását adja vissza.</span><span class="sxs-lookup"><span data-stu-id="75418-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="75418-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75418-114">PARAMETERS</span></span>

### <span data-ttu-id="75418-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75418-115">-DatabaseName</span></span>
<span data-ttu-id="75418-116">Annak az adatbázisnak a nevét adja meg, amelyhez a parancsmag indexjavaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="75418-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="75418-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75418-117">-DefaultProfile</span></span>
<span data-ttu-id="75418-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="75418-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75418-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="75418-119">-IndexRecommendationName</span></span>
<span data-ttu-id="75418-120">Annak az index-javaslatnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="75418-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="75418-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75418-121">-ResourceGroupName</span></span>
<span data-ttu-id="75418-122">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="75418-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="75418-123">Ez a parancsmag indexjavaslatokat kap a kiszolgáló által üzemeltetett adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="75418-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="75418-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="75418-124">-ServerName</span></span>
<span data-ttu-id="75418-125">Azt az adatbázist tartalmazó kiszolgálót adja meg, amelyhez a parancsmag indexelési javaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="75418-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="75418-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="75418-126">-TableName</span></span>
<span data-ttu-id="75418-127">Egy Azure SQL-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75418-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="75418-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75418-128">-Confirm</span></span>
<span data-ttu-id="75418-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75418-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75418-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75418-130">-WhatIf</span></span>
<span data-ttu-id="75418-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75418-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75418-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75418-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75418-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75418-133">CommonParameters</span></span>
<span data-ttu-id="75418-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75418-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75418-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75418-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75418-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75418-136">INPUTS</span></span>

### <span data-ttu-id="75418-137">System.String</span><span class="sxs-lookup"><span data-stu-id="75418-137">System.String</span></span>

## <span data-ttu-id="75418-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75418-138">OUTPUTS</span></span>

### <span data-ttu-id="75418-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="75418-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="75418-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75418-140">NOTES</span></span>

## <span data-ttu-id="75418-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75418-141">RELATED LINKS</span></span>

[<span data-ttu-id="75418-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="75418-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="75418-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="75418-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
