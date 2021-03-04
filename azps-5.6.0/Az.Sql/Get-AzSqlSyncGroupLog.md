---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 40a269ab3d8378ce2f5a2024baee5bca18fe2134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937330"
---
# <span data-ttu-id="9293f-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="9293f-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="9293f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9293f-102">SYNOPSIS</span></span>
<span data-ttu-id="9293f-103">Egy Azure SQL Database Sync-csoport naplóit adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9293f-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9293f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9293f-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9293f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9293f-105">DESCRIPTION</span></span>
<span data-ttu-id="9293f-106">A **Get-AzSqlSyncGroupLog** parancsmag egy Azure SQL Database Sync-csoport naplóit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="9293f-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9293f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9293f-107">EXAMPLES</span></span>

### <span data-ttu-id="9293f-108">1. példa: Azure SQL Sync-csoport naplóinak lekérte</span><span class="sxs-lookup"><span data-stu-id="9293f-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="9293f-109">Ez a parancs egy Azure SQL Sync-csoport naplóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9293f-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="9293f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9293f-110">PARAMETERS</span></span>

### <span data-ttu-id="9293f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9293f-111">-DatabaseName</span></span>
<span data-ttu-id="9293f-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9293f-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9293f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9293f-113">-DefaultProfile</span></span>
<span data-ttu-id="9293f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9293f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9293f-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9293f-115">-EndTime</span></span>
<span data-ttu-id="9293f-116">A lekérdezni következő naplók záró ideje.</span><span class="sxs-lookup"><span data-stu-id="9293f-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="9293f-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="9293f-117">-LogLevel</span></span>
<span data-ttu-id="9293f-118">A lekérdezéshez használható naplók típusa.</span><span class="sxs-lookup"><span data-stu-id="9293f-118">The type of the logs to query.</span></span>
<span data-ttu-id="9293f-119">Érvényes értékek: "Hiba", "Figyelmeztetés", "Sikeres" és "Mind".</span><span class="sxs-lookup"><span data-stu-id="9293f-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="9293f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9293f-120">-ResourceGroupName</span></span>
<span data-ttu-id="9293f-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9293f-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="9293f-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9293f-122">-ServerName</span></span>
<span data-ttu-id="9293f-123">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="9293f-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9293f-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9293f-124">-StartTime</span></span>
<span data-ttu-id="9293f-125">A lekérdezni kezdhető naplók kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="9293f-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="9293f-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9293f-126">-SyncGroupName</span></span>
<span data-ttu-id="9293f-127">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9293f-127">The sync group name.</span></span>

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

### <span data-ttu-id="9293f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9293f-128">CommonParameters</span></span>
<span data-ttu-id="9293f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9293f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9293f-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9293f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9293f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9293f-131">INPUTS</span></span>

### <span data-ttu-id="9293f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9293f-132">System.String</span></span>

## <span data-ttu-id="9293f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9293f-133">OUTPUTS</span></span>

### <span data-ttu-id="9293f-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="9293f-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="9293f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9293f-135">NOTES</span></span>

## <span data-ttu-id="9293f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9293f-136">RELATED LINKS</span></span>
