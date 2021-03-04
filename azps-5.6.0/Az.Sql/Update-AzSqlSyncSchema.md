---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 394ae4d82437795f62e19b4d0f7a536cdd893da9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939298"
---
# <span data-ttu-id="a982e-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="a982e-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="a982e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a982e-102">SYNOPSIS</span></span>
<span data-ttu-id="a982e-103">Frissítse a szinkronizálási séma szinkronizálási tagadatbázis vagy szinkronizálási központ adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="a982e-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="a982e-104">Be fogja szerezni a legújabb adatbázissémát a valós adatbázisból, majd azt használva frissíti a szinkronizálási metaadat-adatbázis által gyorsítótárazott sémát.</span><span class="sxs-lookup"><span data-stu-id="a982e-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="a982e-105">Ha a "SyncMemberName" érték meg van adva, az frissíti a tagadatbázis-sémát; ha nem, akkor frissíti a központi adatbázissémát.</span><span class="sxs-lookup"><span data-stu-id="a982e-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="a982e-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a982e-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a982e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a982e-107">DESCRIPTION</span></span>
<span data-ttu-id="a982e-108">Az **Update-AzSqlSyncSchema** parancsmag frissíti a szinkronizálási sémát egy szinkronizálási tagadatbázishoz vagy egy szinkronizálási központ adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="a982e-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="a982e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a982e-109">EXAMPLES</span></span>

### <span data-ttu-id="a982e-110">1. példa: A szinkronizálási séma frissítése egy központi adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="a982e-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="a982e-111">Ez a parancs frissíti a szinkronizálási sémát a központi adatbázishoz a szinkronizálási csoport syncGroup01 csoportjában</span><span class="sxs-lookup"><span data-stu-id="a982e-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="a982e-112">2. példa: Tagadatbázis szinkronizálási sémája frissítése</span><span class="sxs-lookup"><span data-stu-id="a982e-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="a982e-113">Ez a parancs frissíti a tagadatbázis szinkronizálási sémáját a szinkronizálási tag syncMember01-ben</span><span class="sxs-lookup"><span data-stu-id="a982e-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="a982e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a982e-114">PARAMETERS</span></span>

### <span data-ttu-id="a982e-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a982e-115">-DatabaseName</span></span>
<span data-ttu-id="a982e-116">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a982e-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a982e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a982e-117">-DefaultProfile</span></span>
<span data-ttu-id="a982e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a982e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a982e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a982e-119">-PassThru</span></span>
<span data-ttu-id="a982e-120">Meghatározza, hogy a szinkronizálási csoport visszatérjen-e, és ez a parancsmag működik-e</span><span class="sxs-lookup"><span data-stu-id="a982e-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="a982e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a982e-121">-ResourceGroupName</span></span>
<span data-ttu-id="a982e-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a982e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a982e-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a982e-123">-ServerName</span></span>
<span data-ttu-id="a982e-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="a982e-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a982e-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a982e-125">-SyncGroupName</span></span>
<span data-ttu-id="a982e-126">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a982e-126">The sync group name.</span></span>

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

### <span data-ttu-id="a982e-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="a982e-127">-SyncMemberName</span></span>
<span data-ttu-id="a982e-128">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="a982e-128">The sync member name.</span></span>

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

### <span data-ttu-id="a982e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a982e-129">-Confirm</span></span>
<span data-ttu-id="a982e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a982e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a982e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a982e-131">-WhatIf</span></span>
<span data-ttu-id="a982e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a982e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a982e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a982e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a982e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a982e-134">CommonParameters</span></span>
<span data-ttu-id="a982e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a982e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a982e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a982e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a982e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a982e-137">INPUTS</span></span>

### <span data-ttu-id="a982e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a982e-138">System.String</span></span>

## <span data-ttu-id="a982e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a982e-139">OUTPUTS</span></span>

### <span data-ttu-id="a982e-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a982e-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a982e-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a982e-141">NOTES</span></span>

## <span data-ttu-id="a982e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a982e-142">RELATED LINKS</span></span>
