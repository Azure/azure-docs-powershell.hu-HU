---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: afaa0446b46fca343b4d53ae491c67ef1ceb923a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501336"
---
# <span data-ttu-id="c9367-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9367-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="c9367-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9367-102">SYNOPSIS</span></span>
<span data-ttu-id="c9367-103">Egy Azure SQL-adatbázis szinkronizálási tagjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="c9367-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9367-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9367-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9367-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9367-105">DESCRIPTION</span></span>
<span data-ttu-id="c9367-106">Az **Update-AzureRmSqlSyncGroup** parancsmag az Azure SQL-adatbázis szinkronizálási tagjainak tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="c9367-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c9367-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9367-107">EXAMPLES</span></span>

### <span data-ttu-id="c9367-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9367-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="c9367-109">Ez a parancs visszaállítja a tag-adatbázis rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="c9367-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="c9367-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9367-110">PARAMETERS</span></span>

### <span data-ttu-id="c9367-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9367-111">-DatabaseName</span></span>
<span data-ttu-id="c9367-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c9367-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9367-113">-DefaultProfile</span></span>
<span data-ttu-id="c9367-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c9367-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="c9367-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="c9367-116">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="c9367-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9367-117">-Name</span></span>
<span data-ttu-id="c9367-118">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="c9367-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9367-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9367-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9367-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c9367-121">-ServerName</span></span>
<span data-ttu-id="c9367-122">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="c9367-122">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c9367-123">-SyncGroupName</span></span>
<span data-ttu-id="c9367-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9367-124">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9367-125">-Confirm</span></span>
<span data-ttu-id="c9367-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9367-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9367-127">-WhatIf</span></span>
<span data-ttu-id="c9367-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9367-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9367-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9367-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9367-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9367-130">CommonParameters</span></span>
<span data-ttu-id="c9367-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9367-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9367-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9367-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9367-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9367-133">INPUTS</span></span>

### <span data-ttu-id="c9367-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="c9367-134">None</span></span>
<span data-ttu-id="c9367-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c9367-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9367-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9367-136">OUTPUTS</span></span>

### <span data-ttu-id="c9367-137">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="c9367-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="c9367-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9367-138">NOTES</span></span>

## <span data-ttu-id="c9367-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9367-139">RELATED LINKS</span></span>

[<span data-ttu-id="c9367-140">Új – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9367-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="c9367-141">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9367-141">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="c9367-142">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9367-142">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

