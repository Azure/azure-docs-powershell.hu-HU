---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846433"
---
# <span data-ttu-id="de441-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="de441-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="de441-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de441-102">SYNOPSIS</span></span>
<span data-ttu-id="de441-103">Egy Azure SQL-adatbázis szinkronizálási tagjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="de441-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="de441-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de441-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de441-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de441-105">DESCRIPTION</span></span>
<span data-ttu-id="de441-106">Az **Update-AzSqlSyncGroup** parancsmag az Azure SQL-adatbázis szinkronizálási tagjainak tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="de441-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="de441-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de441-107">EXAMPLES</span></span>

### <span data-ttu-id="de441-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de441-108">Example 1</span></span>
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

<span data-ttu-id="de441-109">Ez a parancs visszaállítja a tag-adatbázis rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="de441-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="de441-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de441-110">PARAMETERS</span></span>

### <span data-ttu-id="de441-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de441-111">-DatabaseName</span></span>
<span data-ttu-id="de441-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="de441-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="de441-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de441-113">-DefaultProfile</span></span>
<span data-ttu-id="de441-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="de441-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de441-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="de441-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="de441-116">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="de441-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de441-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de441-117">-Name</span></span>
<span data-ttu-id="de441-118">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="de441-118">The sync member name.</span></span>

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

### <span data-ttu-id="de441-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de441-119">-ResourceGroupName</span></span>
<span data-ttu-id="de441-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de441-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="de441-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="de441-121">-ServerName</span></span>
<span data-ttu-id="de441-122">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="de441-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="de441-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="de441-123">-SyncGroupName</span></span>
<span data-ttu-id="de441-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="de441-124">The sync group name.</span></span>

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

### <span data-ttu-id="de441-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de441-125">-Confirm</span></span>
<span data-ttu-id="de441-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de441-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de441-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de441-127">-WhatIf</span></span>
<span data-ttu-id="de441-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de441-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de441-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de441-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de441-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de441-130">CommonParameters</span></span>
<span data-ttu-id="de441-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de441-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de441-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de441-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de441-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de441-133">INPUTS</span></span>

### <span data-ttu-id="de441-134">System. String</span><span class="sxs-lookup"><span data-stu-id="de441-134">System.String</span></span>

## <span data-ttu-id="de441-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de441-135">OUTPUTS</span></span>

### <span data-ttu-id="de441-136">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="de441-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="de441-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de441-137">NOTES</span></span>

## <span data-ttu-id="de441-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de441-138">RELATED LINKS</span></span>

[<span data-ttu-id="de441-139">Új – AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="de441-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="de441-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="de441-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="de441-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="de441-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

