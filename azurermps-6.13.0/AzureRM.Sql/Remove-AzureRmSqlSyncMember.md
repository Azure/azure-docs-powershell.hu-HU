---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: 5ef51d83cf2b4cc43693da1697ee15620db04ff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497248"
---
# <span data-ttu-id="a4f85-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4f85-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="a4f85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4f85-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f85-103">Egy Azure SQL-adatbázis szinkronizálási tagjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a4f85-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4f85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4f85-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f85-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4f85-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f85-106">A **Remove-AzureRmSqlSyncMember** parancsmag eltávolítja az Azure SQL-adatbázis szinkronizálási tagját.</span><span class="sxs-lookup"><span data-stu-id="a4f85-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a4f85-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4f85-107">EXAMPLES</span></span>

### <span data-ttu-id="a4f85-108">1. példa: szinkronizálási tag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a4f85-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="a4f85-109">Ez a parancs eltávolítja a syncMember01 nevű Azure SQL-adatbázis szinkronizálási tagját.</span><span class="sxs-lookup"><span data-stu-id="a4f85-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="a4f85-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4f85-110">PARAMETERS</span></span>

### <span data-ttu-id="a4f85-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4f85-111">-DatabaseName</span></span>
<span data-ttu-id="a4f85-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a4f85-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a4f85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f85-113">-DefaultProfile</span></span>
<span data-ttu-id="a4f85-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a4f85-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4f85-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a4f85-115">-Force</span></span>
<span data-ttu-id="a4f85-116">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="a4f85-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a4f85-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4f85-117">-Name</span></span>
<span data-ttu-id="a4f85-118">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="a4f85-118">The sync member name.</span></span>

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

### <span data-ttu-id="a4f85-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4f85-119">-PassThru</span></span>
<span data-ttu-id="a4f85-120">Azt határozza meg, hogy az eltávolított szinkronizálási tagot adja vissza</span><span class="sxs-lookup"><span data-stu-id="a4f85-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="a4f85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f85-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4f85-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4f85-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4f85-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a4f85-123">-ServerName</span></span>
<span data-ttu-id="a4f85-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="a4f85-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a4f85-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f85-125">-SyncGroupName</span></span>
<span data-ttu-id="a4f85-126">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4f85-126">The sync group name.</span></span>

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

### <span data-ttu-id="a4f85-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4f85-127">-Confirm</span></span>
<span data-ttu-id="a4f85-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4f85-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f85-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f85-129">-WhatIf</span></span>
<span data-ttu-id="a4f85-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4f85-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f85-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4f85-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f85-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f85-132">CommonParameters</span></span>
<span data-ttu-id="a4f85-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4f85-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f85-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f85-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f85-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4f85-135">INPUTS</span></span>

### <span data-ttu-id="a4f85-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a4f85-136">System.String</span></span>

## <span data-ttu-id="a4f85-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4f85-137">OUTPUTS</span></span>

### <span data-ttu-id="a4f85-138">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="a4f85-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="a4f85-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4f85-139">NOTES</span></span>

## <span data-ttu-id="a4f85-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4f85-140">RELATED LINKS</span></span>

[<span data-ttu-id="a4f85-141">Új – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4f85-141">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="a4f85-142">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4f85-142">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="a4f85-143">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a4f85-143">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

