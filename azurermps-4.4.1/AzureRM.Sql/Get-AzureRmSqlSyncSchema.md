---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: ef66de2b12cf0ea723540c392a296d2d1c482505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493329"
---
# <span data-ttu-id="de720-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="de720-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="de720-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de720-102">SYNOPSIS</span></span>
<span data-ttu-id="de720-103">Egy tag-adatbázis vagy egy központi adatbázis szinkronizálási sémájáról szóló információt ad meg.</span><span class="sxs-lookup"><span data-stu-id="de720-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de720-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de720-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de720-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de720-105">DESCRIPTION</span></span>
<span data-ttu-id="de720-106">A **Get-AzureRmSqlSyncSchema** parancsmag egy tag-adatbázis vagy egy központi adatbázis szinkronizálási sémájáról ad információt.</span><span class="sxs-lookup"><span data-stu-id="de720-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="de720-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de720-107">EXAMPLES</span></span>

### <span data-ttu-id="de720-108">Példa 1,1: a Szinkronizáló séma beszerzése központi adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="de720-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="de720-109">Ez a parancs a központi adatbázis szinkronizálási sémáját a szinkronizálás csoport syncGroup01 kapja.</span><span class="sxs-lookup"><span data-stu-id="de720-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="de720-110">Példa 1,2: a központi adatbázis szinkronizálási sémájának beszerzése és a táblázatok kibontása</span><span class="sxs-lookup"><span data-stu-id="de720-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="de720-111">Ez a parancs a központi adatbázis szinkronizálási sémáját a szinkronizálás csoport syncGroup01 és a Tables tulajdonság kibontásával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="de720-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="de720-112">2. példa: a szinkronizálási séma beszerzése egy tag adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="de720-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="de720-113">Ez a parancs a szinkronizálási tag syncMember01 a tagsági adatbázis szinkronizálási sémáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="de720-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="de720-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de720-114">PARAMETERS</span></span>

### <span data-ttu-id="de720-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de720-115">-DatabaseName</span></span>
<span data-ttu-id="de720-116">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="de720-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="de720-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de720-117">-ResourceGroupName</span></span>
<span data-ttu-id="de720-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de720-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="de720-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="de720-119">-ServerName</span></span>
<span data-ttu-id="de720-120">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="de720-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="de720-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="de720-121">-SyncGroupName</span></span>
<span data-ttu-id="de720-122">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="de720-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de720-123">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="de720-123">-SyncMemberName</span></span>
<span data-ttu-id="de720-124">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="de720-124">The sync member name.</span></span>

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

### <span data-ttu-id="de720-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de720-125">-DefaultProfile</span></span>
<span data-ttu-id="de720-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de720-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de720-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de720-127">CommonParameters</span></span>
<span data-ttu-id="de720-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de720-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de720-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de720-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de720-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de720-130">INPUTS</span></span>

## <span data-ttu-id="de720-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de720-131">OUTPUTS</span></span>

### <span data-ttu-id="de720-132">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="de720-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="de720-133">Táblázatok: Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncFullSchemaTableModel</span><span class="sxs-lookup"><span data-stu-id="de720-133">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="de720-134">Columns: Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncFullSchemaColumnModel</span><span class="sxs-lookup"><span data-stu-id="de720-134">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="de720-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de720-135">NOTES</span></span>

## <span data-ttu-id="de720-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de720-136">RELATED LINKS</span></span>

