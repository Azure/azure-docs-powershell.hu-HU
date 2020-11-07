---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5f0786c180461522d17d2697931f4a9887935f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679921"
---
# <span data-ttu-id="9d34d-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="9d34d-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="9d34d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d34d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d34d-103">Az Azure SQL adatbázis-kiszolgáló szolgáltatási céljainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="9d34d-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d34d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d34d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d34d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d34d-105">DESCRIPTION</span></span>
<span data-ttu-id="9d34d-106">A **Get-AzureRmSqlServerServiceObjective** parancsmag elérhetővé válik az Azure SQL adatbázis-kiszolgálók elérhető szolgáltatási céljainak.</span><span class="sxs-lookup"><span data-stu-id="9d34d-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="9d34d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d34d-107">EXAMPLES</span></span>

### <span data-ttu-id="9d34d-108">Példa 1: szolgáltatási célok beszerzése</span><span class="sxs-lookup"><span data-stu-id="9d34d-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="9d34d-109">Ez a parancs a Server01 és a Database01 nevű adatbázis szolgáltatási céljait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d34d-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="9d34d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d34d-110">PARAMETERS</span></span>

### <span data-ttu-id="9d34d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9d34d-111">-DatabaseName</span></span>
<span data-ttu-id="9d34d-112">Egy Azure SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d34d-112">Specifies the name of an Azure SQL Database.</span></span>

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

### <span data-ttu-id="9d34d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d34d-113">-ResourceGroupName</span></span>
<span data-ttu-id="9d34d-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d34d-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9d34d-115">Ez a parancsmag az erőforráshoz rendelt SQL-adatbázis-kiszolgáló szolgáltatási céljait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d34d-115">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="9d34d-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="9d34d-116">-ServerName</span></span>
<span data-ttu-id="9d34d-117">Egy SQL-adatbázis SQL Server-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d34d-117">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="9d34d-118">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9d34d-118">-ServiceObjectiveName</span></span>
<span data-ttu-id="9d34d-119">Itt adhatja meg az Azure SQL-adatbázis-kiszolgáló szolgáltatási céljainak a nevét.</span><span class="sxs-lookup"><span data-stu-id="9d34d-119">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="9d34d-120">A paraméter elfogadható értékei a következők: Basic, S0, S1, S2, P1, P2 és P3.</span><span class="sxs-lookup"><span data-stu-id="9d34d-120">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="9d34d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d34d-121">-Confirm</span></span>
<span data-ttu-id="9d34d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d34d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d34d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d34d-123">-WhatIf</span></span>
<span data-ttu-id="9d34d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d34d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d34d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d34d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d34d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d34d-126">-DefaultProfile</span></span>
<span data-ttu-id="9d34d-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d34d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d34d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d34d-128">CommonParameters</span></span>
<span data-ttu-id="9d34d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d34d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d34d-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d34d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d34d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d34d-131">INPUTS</span></span>

## <span data-ttu-id="9d34d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d34d-132">OUTPUTS</span></span>

### <span data-ttu-id="9d34d-133">Microsoft. Azure. Command. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="9d34d-133">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="9d34d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d34d-134">NOTES</span></span>

## <span data-ttu-id="9d34d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d34d-135">RELATED LINKS</span></span>

[<span data-ttu-id="9d34d-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9d34d-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


