---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846421"
---
# <span data-ttu-id="1d52c-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="1d52c-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="1d52c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d52c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d52c-103">Frissítheti a Szinkronizáló sémát egy szinkronizálási tag-adatbázishoz vagy egy szinkronizáló központi adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="1d52c-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="1d52c-104">A legújabb adatbázis-séma a valós adatbázisból fog megjelenni, majd a szinkronizálási metaadat-adatbázis segítségével frissíti a sémát.</span><span class="sxs-lookup"><span data-stu-id="1d52c-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="1d52c-105">Ha a "SyncMemberName" érték van megadva, a program frissíti a tag adatbázis-sémát; Ha nem, akkor frissíti a központi adatbázis-sémát.</span><span class="sxs-lookup"><span data-stu-id="1d52c-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="1d52c-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d52c-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d52c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d52c-107">DESCRIPTION</span></span>
<span data-ttu-id="1d52c-108">Az **Update-AzSqlSyncSchema** parancsmag frissíti a Szinkronizáló sémát egy szinkronizáló vagy egy szinkronizáló központi adatbázis esetében.</span><span class="sxs-lookup"><span data-stu-id="1d52c-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="1d52c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1d52c-109">EXAMPLES</span></span>

### <span data-ttu-id="1d52c-110">Példa 1: a központi adatbázis szinkronizálási sémájának frissítése</span><span class="sxs-lookup"><span data-stu-id="1d52c-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="1d52c-111">A parancs frissíti a központi adatbázis szinkronizálási sémáját a szinkronizálás csoport syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="1d52c-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="1d52c-112">2. példa: a szinkronizálási séma frissítése a tagok adatbázisaiban</span><span class="sxs-lookup"><span data-stu-id="1d52c-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="1d52c-113">Ez a parancs frissíti a tagsági adatbázis szinkronizálási sémáját a szinkronizálási tagok syncMember01</span><span class="sxs-lookup"><span data-stu-id="1d52c-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="1d52c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d52c-114">PARAMETERS</span></span>

### <span data-ttu-id="1d52c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d52c-115">-DatabaseName</span></span>
<span data-ttu-id="1d52c-116">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1d52c-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1d52c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d52c-117">-DefaultProfile</span></span>
<span data-ttu-id="1d52c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1d52c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d52c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d52c-119">-PassThru</span></span>
<span data-ttu-id="1d52c-120">Meghatározza, hogy a szinkronizálási csoport visszaadja-e a parancsmagot</span><span class="sxs-lookup"><span data-stu-id="1d52c-120">Defines Whether return the sync group this cmdlet works on</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d52c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d52c-121">-ResourceGroupName</span></span>
<span data-ttu-id="1d52c-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1d52c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="1d52c-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1d52c-123">-ServerName</span></span>
<span data-ttu-id="1d52c-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="1d52c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1d52c-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1d52c-125">-SyncGroupName</span></span>
<span data-ttu-id="1d52c-126">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1d52c-126">The sync group name.</span></span>

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

### <span data-ttu-id="1d52c-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="1d52c-127">-SyncMemberName</span></span>
<span data-ttu-id="1d52c-128">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="1d52c-128">The sync member name.</span></span>

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

### <span data-ttu-id="1d52c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d52c-129">-Confirm</span></span>
<span data-ttu-id="1d52c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d52c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d52c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d52c-131">-WhatIf</span></span>
<span data-ttu-id="1d52c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d52c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d52c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d52c-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d52c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d52c-134">CommonParameters</span></span>
<span data-ttu-id="1d52c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d52c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d52c-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d52c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d52c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d52c-137">INPUTS</span></span>

### <span data-ttu-id="1d52c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1d52c-138">System.String</span></span>

## <span data-ttu-id="1d52c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d52c-139">OUTPUTS</span></span>

### <span data-ttu-id="1d52c-140">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="1d52c-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1d52c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d52c-141">NOTES</span></span>

## <span data-ttu-id="1d52c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d52c-142">RELATED LINKS</span></span>
