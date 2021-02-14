---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163226"
---
# <span data-ttu-id="43d0f-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="43d0f-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="43d0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="43d0f-103">Eltávolít egy Azure SQL Database Sync- tagot.</span><span class="sxs-lookup"><span data-stu-id="43d0f-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="43d0f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43d0f-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43d0f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="43d0f-106">A **Remove-AzSqlSyncMember** parancsmag eltávolítja az Azure SQL Database Sync tagját.</span><span class="sxs-lookup"><span data-stu-id="43d0f-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="43d0f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="43d0f-108">1. példa: Szinkronizálási tag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="43d0f-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="43d0f-109">Ez a parancs eltávolítja a syncMember01 nevű Azure SQL Database Sync membert.</span><span class="sxs-lookup"><span data-stu-id="43d0f-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="43d0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="43d0f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="43d0f-111">-DatabaseName</span></span>
<span data-ttu-id="43d0f-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="43d0f-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="43d0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d0f-113">-DefaultProfile</span></span>
<span data-ttu-id="43d0f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43d0f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43d0f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="43d0f-115">-Force</span></span>
<span data-ttu-id="43d0f-116">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="43d0f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="43d0f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43d0f-117">-Name</span></span>
<span data-ttu-id="43d0f-118">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="43d0f-118">The sync member name.</span></span>

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

### <span data-ttu-id="43d0f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43d0f-119">-PassThru</span></span>
<span data-ttu-id="43d0f-120">Meghatározza, hogy visszaadja-e az eltávolított szinkronizálási tagot</span><span class="sxs-lookup"><span data-stu-id="43d0f-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="43d0f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d0f-121">-ResourceGroupName</span></span>
<span data-ttu-id="43d0f-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43d0f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="43d0f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43d0f-123">-ServerName</span></span>
<span data-ttu-id="43d0f-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="43d0f-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="43d0f-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="43d0f-125">-SyncGroupName</span></span>
<span data-ttu-id="43d0f-126">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="43d0f-126">The sync group name.</span></span>

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

### <span data-ttu-id="43d0f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43d0f-127">-Confirm</span></span>
<span data-ttu-id="43d0f-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43d0f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d0f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d0f-129">-WhatIf</span></span>
<span data-ttu-id="43d0f-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43d0f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d0f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43d0f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d0f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d0f-132">CommonParameters</span></span>
<span data-ttu-id="43d0f-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d0f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d0f-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43d0f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d0f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43d0f-135">INPUTS</span></span>

### <span data-ttu-id="43d0f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="43d0f-136">System.String</span></span>

## <span data-ttu-id="43d0f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43d0f-137">OUTPUTS</span></span>

### <span data-ttu-id="43d0f-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="43d0f-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="43d0f-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43d0f-139">NOTES</span></span>

## <span data-ttu-id="43d0f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43d0f-140">RELATED LINKS</span></span>

[<span data-ttu-id="43d0f-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="43d0f-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="43d0f-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="43d0f-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="43d0f-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="43d0f-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

