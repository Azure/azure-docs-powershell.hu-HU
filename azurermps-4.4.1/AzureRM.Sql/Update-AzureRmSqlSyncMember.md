---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: f72091d142b57cc7ef3897eceda2219634376daf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673093"
---
# <span data-ttu-id="1050b-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1050b-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="1050b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1050b-102">SYNOPSIS</span></span>
<span data-ttu-id="1050b-103">Egy Azure SQL-adatbázis szinkronizálási tagjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="1050b-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1050b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1050b-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1050b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1050b-105">DESCRIPTION</span></span>
<span data-ttu-id="1050b-106">Az **Update-AzureRmSqlSyncGroup** parancsmag az Azure SQL-adatbázis szinkronizálási tagjainak tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="1050b-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="1050b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1050b-107">EXAMPLES</span></span>

### <span data-ttu-id="1050b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1050b-108">Example 1</span></span>
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

<span data-ttu-id="1050b-109">Ez a parancs visszaállítja a tag-adatbázis rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="1050b-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="1050b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1050b-110">PARAMETERS</span></span>

### <span data-ttu-id="1050b-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1050b-111">-Confirm</span></span>
<span data-ttu-id="1050b-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1050b-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1050b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1050b-113">-DatabaseName</span></span>
<span data-ttu-id="1050b-114">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1050b-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1050b-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="1050b-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="1050b-116">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="1050b-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1050b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1050b-117">-Name</span></span>
<span data-ttu-id="1050b-118">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="1050b-118">The sync member name.</span></span>

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

### <span data-ttu-id="1050b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1050b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1050b-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1050b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1050b-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1050b-121">-ServerName</span></span>
<span data-ttu-id="1050b-122">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="1050b-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1050b-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1050b-123">-SyncGroupName</span></span>
<span data-ttu-id="1050b-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1050b-124">The sync group name.</span></span>

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

### <span data-ttu-id="1050b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1050b-125">-WhatIf</span></span>
<span data-ttu-id="1050b-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1050b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1050b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1050b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1050b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1050b-128">-DefaultProfile</span></span>
<span data-ttu-id="1050b-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1050b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1050b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1050b-130">CommonParameters</span></span>
<span data-ttu-id="1050b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1050b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1050b-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1050b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1050b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1050b-133">INPUTS</span></span>

## <span data-ttu-id="1050b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1050b-134">OUTPUTS</span></span>

### <span data-ttu-id="1050b-135">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="1050b-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="1050b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1050b-136">NOTES</span></span>

## <span data-ttu-id="1050b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1050b-137">RELATED LINKS</span></span>

[<span data-ttu-id="1050b-138">Új – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1050b-138">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="1050b-139">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1050b-139">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="1050b-140">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1050b-140">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

