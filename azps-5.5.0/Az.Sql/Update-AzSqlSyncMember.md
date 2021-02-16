---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155171"
---
# <span data-ttu-id="ba438-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba438-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="ba438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba438-102">SYNOPSIS</span></span>
<span data-ttu-id="ba438-103">Frissíti az Azure SQL Database Sync egyik tagját.</span><span class="sxs-lookup"><span data-stu-id="ba438-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ba438-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba438-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba438-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba438-105">DESCRIPTION</span></span>
<span data-ttu-id="ba438-106">Az **Update-AzSqlSyncGroup** parancsmag módosítja egy Azure SQL Database Sync-tag tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ba438-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ba438-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba438-107">EXAMPLES</span></span>

### <span data-ttu-id="ba438-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ba438-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="ba438-109">Ez a parancs alaphelyzetbe állítja a tagadatbázis rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="ba438-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="ba438-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba438-110">PARAMETERS</span></span>

### <span data-ttu-id="ba438-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba438-111">-DatabaseName</span></span>
<span data-ttu-id="ba438-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ba438-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ba438-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba438-113">-DefaultProfile</span></span>
<span data-ttu-id="ba438-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba438-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba438-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ba438-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="ba438-116">Az Azure SQL-adatbázis hitelesítő adatai (felhasználóneve és jelszava).</span><span class="sxs-lookup"><span data-stu-id="ba438-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba438-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ba438-117">-Name</span></span>
<span data-ttu-id="ba438-118">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="ba438-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba438-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba438-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba438-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba438-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba438-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba438-121">-ServerName</span></span>
<span data-ttu-id="ba438-122">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="ba438-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ba438-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ba438-123">-SyncGroupName</span></span>
<span data-ttu-id="ba438-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba438-124">The sync group name.</span></span>

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

### <span data-ttu-id="ba438-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ba438-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="ba438-126">A szinkronizálási tagadatbázis erőforrás-azonosítója, ha a UsePrivateLinkConnection igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="ba438-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba438-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ba438-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="ba438-128">Hogy a szinkronizálási taghoz való csatlakozáskor használjon-e privát hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="ba438-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba438-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba438-129">-Confirm</span></span>
<span data-ttu-id="ba438-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ba438-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba438-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba438-131">-WhatIf</span></span>
<span data-ttu-id="ba438-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ba438-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba438-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba438-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba438-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba438-134">CommonParameters</span></span>
<span data-ttu-id="ba438-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba438-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba438-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba438-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba438-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba438-137">INPUTS</span></span>

### <span data-ttu-id="ba438-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ba438-138">System.String</span></span>

## <span data-ttu-id="ba438-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba438-139">OUTPUTS</span></span>

### <span data-ttu-id="ba438-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ba438-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ba438-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba438-141">NOTES</span></span>

## <span data-ttu-id="ba438-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba438-142">RELATED LINKS</span></span>

[<span data-ttu-id="ba438-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba438-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="ba438-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba438-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="ba438-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba438-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

