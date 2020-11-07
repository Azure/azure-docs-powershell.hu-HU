---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 0343cddd12fdf1fe438ec2c4c9c3c5763719cd43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839434"
---
# <span data-ttu-id="e58d6-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="e58d6-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="e58d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e58d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e58d6-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e58d6-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e58d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e58d6-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e58d6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e58d6-105">DESCRIPTION</span></span>
<span data-ttu-id="e58d6-106">A **Get-AzSqlSyncGroupLog** parancsmag egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e58d6-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e58d6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e58d6-107">EXAMPLES</span></span>

### <span data-ttu-id="e58d6-108">1. példa: az Azure SQL szinkronizálási csoport naplóinak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e58d6-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="e58d6-109">Ez a parancs beolvassa az Azure SQL szinkronizálási csoport naplóit.</span><span class="sxs-lookup"><span data-stu-id="e58d6-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="e58d6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e58d6-110">PARAMETERS</span></span>

### <span data-ttu-id="e58d6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e58d6-111">-DatabaseName</span></span>
<span data-ttu-id="e58d6-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e58d6-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e58d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e58d6-113">-DefaultProfile</span></span>
<span data-ttu-id="e58d6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e58d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e58d6-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="e58d6-115">-EndTime</span></span>
<span data-ttu-id="e58d6-116">A lekérdezni kívánt naplók befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="e58d6-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="e58d6-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="e58d6-117">-LogLevel</span></span>
<span data-ttu-id="e58d6-118">A lekérdezni kívánt naplók típusa.</span><span class="sxs-lookup"><span data-stu-id="e58d6-118">The type of the logs to query.</span></span>
<span data-ttu-id="e58d6-119">Az érvényes értékek a következők: "hiba", "figyelmeztetés", "siker" és "mind".</span><span class="sxs-lookup"><span data-stu-id="e58d6-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="e58d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e58d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="e58d6-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e58d6-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e58d6-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e58d6-122">-ServerName</span></span>
<span data-ttu-id="e58d6-123">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="e58d6-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e58d6-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="e58d6-124">-StartTime</span></span>
<span data-ttu-id="e58d6-125">A lekérdezni kívánt naplók kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="e58d6-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="e58d6-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e58d6-126">-SyncGroupName</span></span>
<span data-ttu-id="e58d6-127">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e58d6-127">The sync group name.</span></span>

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

### <span data-ttu-id="e58d6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e58d6-128">CommonParameters</span></span>
<span data-ttu-id="e58d6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e58d6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e58d6-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e58d6-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e58d6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e58d6-131">INPUTS</span></span>

### <span data-ttu-id="e58d6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e58d6-132">System.String</span></span>

## <span data-ttu-id="e58d6-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e58d6-133">OUTPUTS</span></span>

### <span data-ttu-id="e58d6-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="e58d6-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="e58d6-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e58d6-135">NOTES</span></span>

## <span data-ttu-id="e58d6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e58d6-136">RELATED LINKS</span></span>
