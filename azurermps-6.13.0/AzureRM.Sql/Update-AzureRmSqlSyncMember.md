---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: 7737baa8459cc9acae86cbd3e632dd73f9433056
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502823"
---
# <span data-ttu-id="8569e-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8569e-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="8569e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8569e-102">SYNOPSIS</span></span>
<span data-ttu-id="8569e-103">Egy Azure SQL-adatbázis szinkronizálási tagjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="8569e-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8569e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8569e-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8569e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8569e-105">DESCRIPTION</span></span>
<span data-ttu-id="8569e-106">Az **Update-AzureRmSqlSyncGroup** parancsmag az Azure SQL-adatbázis szinkronizálási tagjainak tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="8569e-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="8569e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8569e-107">EXAMPLES</span></span>

### <span data-ttu-id="8569e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8569e-108">Example 1</span></span>
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

<span data-ttu-id="8569e-109">Ez a parancs visszaállítja a tag-adatbázis rendszergazdai jelszavát.</span><span class="sxs-lookup"><span data-stu-id="8569e-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="8569e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8569e-110">PARAMETERS</span></span>

### <span data-ttu-id="8569e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8569e-111">-DatabaseName</span></span>
<span data-ttu-id="8569e-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="8569e-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8569e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8569e-113">-DefaultProfile</span></span>
<span data-ttu-id="8569e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8569e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8569e-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="8569e-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="8569e-116">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="8569e-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8569e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8569e-117">-Name</span></span>
<span data-ttu-id="8569e-118">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="8569e-118">The sync member name.</span></span>

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

### <span data-ttu-id="8569e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8569e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8569e-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8569e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8569e-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8569e-121">-ServerName</span></span>
<span data-ttu-id="8569e-122">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="8569e-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="8569e-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8569e-123">-SyncGroupName</span></span>
<span data-ttu-id="8569e-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8569e-124">The sync group name.</span></span>

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

### <span data-ttu-id="8569e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8569e-125">-Confirm</span></span>
<span data-ttu-id="8569e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8569e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8569e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8569e-127">-WhatIf</span></span>
<span data-ttu-id="8569e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8569e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8569e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8569e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8569e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8569e-130">CommonParameters</span></span>
<span data-ttu-id="8569e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8569e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8569e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8569e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8569e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8569e-133">INPUTS</span></span>

### <span data-ttu-id="8569e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8569e-134">System.String</span></span>

## <span data-ttu-id="8569e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8569e-135">OUTPUTS</span></span>

### <span data-ttu-id="8569e-136">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="8569e-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="8569e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8569e-137">NOTES</span></span>

## <span data-ttu-id="8569e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8569e-138">RELATED LINKS</span></span>

[<span data-ttu-id="8569e-139">Új – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8569e-139">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="8569e-140">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8569e-140">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="8569e-141">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8569e-141">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

