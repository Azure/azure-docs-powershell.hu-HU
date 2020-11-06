---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: 924e00578383e103d1451e311d027edd02752496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493332"
---
# <span data-ttu-id="0def0-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="0def0-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="0def0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0def0-102">SYNOPSIS</span></span>
<span data-ttu-id="0def0-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0def0-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0def0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0def0-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0def0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0def0-105">DESCRIPTION</span></span>
<span data-ttu-id="0def0-106">A **Get-AzureRmSqlSyncGroupLog** parancsmag egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0def0-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0def0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0def0-107">EXAMPLES</span></span>

### <span data-ttu-id="0def0-108">1. példa: az Azure SQL szinkronizálási csoport naplóinak beolvasása</span><span class="sxs-lookup"><span data-stu-id="0def0-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="0def0-109">Ez a parancs beolvassa az Azure SQL szinkronizálási csoport naplóit.</span><span class="sxs-lookup"><span data-stu-id="0def0-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="0def0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0def0-110">PARAMETERS</span></span>

### <span data-ttu-id="0def0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0def0-111">-DatabaseName</span></span>
<span data-ttu-id="0def0-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0def0-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0def0-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="0def0-113">-EndTime</span></span>
<span data-ttu-id="0def0-114">A lekérdezni kívánt naplók befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="0def0-114">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0def0-115">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="0def0-115">-LogLevel</span></span>
<span data-ttu-id="0def0-116">A lekérdezni kívánt naplók típusa.</span><span class="sxs-lookup"><span data-stu-id="0def0-116">The type of the logs to query.</span></span>
<span data-ttu-id="0def0-117">Az érvényes értékek a következők: "hiba", "figyelmeztetés", "siker" és "mind".</span><span class="sxs-lookup"><span data-stu-id="0def0-117">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0def0-118">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0def0-118">-SyncGroupName</span></span>
<span data-ttu-id="0def0-119">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0def0-119">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0def0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0def0-120">-ResourceGroupName</span></span>
<span data-ttu-id="0def0-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0def0-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="0def0-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0def0-122">-ServerName</span></span>
<span data-ttu-id="0def0-123">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="0def0-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0def0-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="0def0-124">-StartTime</span></span>
<span data-ttu-id="0def0-125">A lekérdezni kívánt naplók kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="0def0-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0def0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0def0-126">-DefaultProfile</span></span>
<span data-ttu-id="0def0-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0def0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0def0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0def0-128">CommonParameters</span></span>
<span data-ttu-id="0def0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0def0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0def0-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0def0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0def0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0def0-131">INPUTS</span></span>

## <span data-ttu-id="0def0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0def0-132">OUTPUTS</span></span>

### <span data-ttu-id="0def0-133">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="0def0-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="0def0-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0def0-134">NOTES</span></span>

## <span data-ttu-id="0def0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0def0-135">RELATED LINKS</span></span>

