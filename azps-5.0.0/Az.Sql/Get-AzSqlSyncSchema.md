---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7dc07f1064837b710c246e4aafb4ceb008019e4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185663"
---
# <span data-ttu-id="a0beb-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="a0beb-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="a0beb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0beb-102">SYNOPSIS</span></span>
<span data-ttu-id="a0beb-103">Egy tag-adatbázis vagy egy központi adatbázis szinkronizálási sémájáról szóló információt ad meg.</span><span class="sxs-lookup"><span data-stu-id="a0beb-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="a0beb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0beb-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0beb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0beb-105">DESCRIPTION</span></span>
<span data-ttu-id="a0beb-106">A **Get-AzSqlSyncSchema** parancsmag egy tag-adatbázis vagy egy központi adatbázis szinkronizálási sémájáról ad információt.</span><span class="sxs-lookup"><span data-stu-id="a0beb-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="a0beb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0beb-107">EXAMPLES</span></span>

### <span data-ttu-id="a0beb-108">Példa 1: a Szinkronizáló séma beszerzése központi adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="a0beb-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="a0beb-109">Ez a parancs a központi adatbázis szinkronizálási sémáját a szinkronizálás csoport syncGroup01 kapja.</span><span class="sxs-lookup"><span data-stu-id="a0beb-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="a0beb-110">2. példa: a Szinkronizáló séma beszerzése egy központi adatbázishoz és a táblázatok kibontása</span><span class="sxs-lookup"><span data-stu-id="a0beb-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="a0beb-111">Ez a parancs a központi adatbázis szinkronizálási sémáját a szinkronizálás csoport syncGroup01 és a Tables tulajdonság kibontásával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0beb-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="a0beb-112">3. példa: a szinkronizálási séma beszerzése egy tag-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="a0beb-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="a0beb-113">Ez a parancs a szinkronizálási tag syncMember01 a tagsági adatbázis szinkronizálási sémáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0beb-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="a0beb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0beb-114">PARAMETERS</span></span>

### <span data-ttu-id="a0beb-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0beb-115">-DatabaseName</span></span>
<span data-ttu-id="a0beb-116">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a0beb-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a0beb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0beb-117">-DefaultProfile</span></span>
<span data-ttu-id="a0beb-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0beb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0beb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0beb-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0beb-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a0beb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0beb-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a0beb-121">-ServerName</span></span>
<span data-ttu-id="a0beb-122">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="a0beb-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a0beb-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a0beb-123">-SyncGroupName</span></span>
<span data-ttu-id="a0beb-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a0beb-124">The sync group name.</span></span>

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

### <span data-ttu-id="a0beb-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="a0beb-125">-SyncMemberName</span></span>
<span data-ttu-id="a0beb-126">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="a0beb-126">The sync member name.</span></span>

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

### <span data-ttu-id="a0beb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0beb-127">CommonParameters</span></span>
<span data-ttu-id="a0beb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0beb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0beb-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a0beb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0beb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0beb-130">INPUTS</span></span>

### <span data-ttu-id="a0beb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a0beb-131">System.String</span></span>

## <span data-ttu-id="a0beb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0beb-132">OUTPUTS</span></span>

### <span data-ttu-id="a0beb-133">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="a0beb-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="a0beb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0beb-134">NOTES</span></span>

## <span data-ttu-id="a0beb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0beb-135">RELATED LINKS</span></span>