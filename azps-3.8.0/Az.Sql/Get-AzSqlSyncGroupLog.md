---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010764"
---
# <span data-ttu-id="2a9a9-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="2a9a9-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="2a9a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9a9-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2a9a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a9a9-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a9a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="2a9a9-106">A **Get-AzSqlSyncGroupLog** parancsmag egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2a9a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2a9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="2a9a9-108">1. példa: az Azure SQL szinkronizálási csoport naplóinak beolvasása</span><span class="sxs-lookup"><span data-stu-id="2a9a9-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="2a9a9-109">Ez a parancs beolvassa az Azure SQL szinkronizálási csoport naplóit.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="2a9a9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a9a9-110">PARAMETERS</span></span>

### <span data-ttu-id="2a9a9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a9a9-111">-DatabaseName</span></span>
<span data-ttu-id="2a9a9-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2a9a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9a9-113">-DefaultProfile</span></span>
<span data-ttu-id="2a9a9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2a9a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a9a9-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="2a9a9-115">-EndTime</span></span>
<span data-ttu-id="2a9a9-116">A lekérdezni kívánt naplók befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="2a9a9-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="2a9a9-117">-LogLevel</span></span>
<span data-ttu-id="2a9a9-118">A lekérdezni kívánt naplók típusa.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-118">The type of the logs to query.</span></span>
<span data-ttu-id="2a9a9-119">Az érvényes értékek a következők: "hiba", "figyelmeztetés", "siker" és "mind".</span><span class="sxs-lookup"><span data-stu-id="2a9a9-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="2a9a9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a9a9-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a9a9-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a9a9-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2a9a9-122">-ServerName</span></span>
<span data-ttu-id="2a9a9-123">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2a9a9-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="2a9a9-124">-StartTime</span></span>
<span data-ttu-id="2a9a9-125">A lekérdezni kívánt naplók kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="2a9a9-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2a9a9-126">-SyncGroupName</span></span>
<span data-ttu-id="2a9a9-127">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-127">The sync group name.</span></span>

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

### <span data-ttu-id="2a9a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9a9-128">CommonParameters</span></span>
<span data-ttu-id="2a9a9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a9a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9a9-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2a9a9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9a9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a9a9-131">INPUTS</span></span>

### <span data-ttu-id="2a9a9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2a9a9-132">System.String</span></span>

## <span data-ttu-id="2a9a9-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a9a9-133">OUTPUTS</span></span>

### <span data-ttu-id="2a9a9-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="2a9a9-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="2a9a9-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a9a9-135">NOTES</span></span>

## <span data-ttu-id="2a9a9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a9a9-136">RELATED LINKS</span></span>
