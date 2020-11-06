---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: 09d095751ff9f9e8ba7103073392f2c2d0a008d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502875"
---
# <span data-ttu-id="fcc99-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="fcc99-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="fcc99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcc99-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc99-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="fcc99-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcc99-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcc99-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcc99-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc99-106">A **Get-AzureRmSqlSyncGroupLog** parancsmag egy Azure SQL-adatbázis szinkronizálási csoportjának naplóit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="fcc99-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fcc99-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fcc99-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc99-108">1. példa: az Azure SQL szinkronizálási csoport naplóinak beolvasása</span><span class="sxs-lookup"><span data-stu-id="fcc99-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="fcc99-109">Ez a parancs beolvassa az Azure SQL szinkronizálási csoport naplóit.</span><span class="sxs-lookup"><span data-stu-id="fcc99-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="fcc99-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcc99-110">PARAMETERS</span></span>

### <span data-ttu-id="fcc99-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fcc99-111">-DatabaseName</span></span>
<span data-ttu-id="fcc99-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fcc99-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="fcc99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc99-113">-DefaultProfile</span></span>
<span data-ttu-id="fcc99-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fcc99-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcc99-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="fcc99-115">-EndTime</span></span>
<span data-ttu-id="fcc99-116">A lekérdezni kívánt naplók befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="fcc99-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="fcc99-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="fcc99-117">-LogLevel</span></span>
<span data-ttu-id="fcc99-118">A lekérdezni kívánt naplók típusa.</span><span class="sxs-lookup"><span data-stu-id="fcc99-118">The type of the logs to query.</span></span>
<span data-ttu-id="fcc99-119">Az érvényes értékek a következők: "hiba", "figyelmeztetés", "siker" és "mind".</span><span class="sxs-lookup"><span data-stu-id="fcc99-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="fcc99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc99-120">-ResourceGroupName</span></span>
<span data-ttu-id="fcc99-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fcc99-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="fcc99-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fcc99-122">-ServerName</span></span>
<span data-ttu-id="fcc99-123">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="fcc99-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fcc99-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="fcc99-124">-StartTime</span></span>
<span data-ttu-id="fcc99-125">A lekérdezni kívánt naplók kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="fcc99-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="fcc99-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc99-126">-SyncGroupName</span></span>
<span data-ttu-id="fcc99-127">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fcc99-127">The sync group name.</span></span>

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

### <span data-ttu-id="fcc99-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc99-128">CommonParameters</span></span>
<span data-ttu-id="fcc99-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcc99-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc99-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc99-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc99-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcc99-131">INPUTS</span></span>

### <span data-ttu-id="fcc99-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fcc99-132">System.String</span></span>

## <span data-ttu-id="fcc99-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcc99-133">OUTPUTS</span></span>

### <span data-ttu-id="fcc99-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="fcc99-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="fcc99-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcc99-135">NOTES</span></span>

## <span data-ttu-id="fcc99-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcc99-136">RELATED LINKS</span></span>
