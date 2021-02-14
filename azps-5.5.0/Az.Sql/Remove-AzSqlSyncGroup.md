---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163243"
---
# <span data-ttu-id="fab07-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fab07-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="fab07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab07-102">SYNOPSIS</span></span>
<span data-ttu-id="fab07-103">Eltávolít egy Azure SQL Database Sync-csoportot.</span><span class="sxs-lookup"><span data-stu-id="fab07-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fab07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fab07-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fab07-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fab07-105">DESCRIPTION</span></span>
<span data-ttu-id="fab07-106">A **Remove-AzSqlSyncGroup** parancsmag eltávolít egy Azure SQL Database Sync-csoportot.</span><span class="sxs-lookup"><span data-stu-id="fab07-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fab07-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fab07-107">EXAMPLES</span></span>

### <span data-ttu-id="fab07-108">1. példa: Szinkronizálási csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fab07-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="fab07-109">Ez a parancs eltávolítja a syncGroup01 nevű Azure SQL Database Sync-csoportot.</span><span class="sxs-lookup"><span data-stu-id="fab07-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="fab07-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fab07-110">PARAMETERS</span></span>

### <span data-ttu-id="fab07-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fab07-111">-DatabaseName</span></span>
<span data-ttu-id="fab07-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fab07-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="fab07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab07-113">-DefaultProfile</span></span>
<span data-ttu-id="fab07-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fab07-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fab07-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fab07-115">-Force</span></span>
<span data-ttu-id="fab07-116">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="fab07-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fab07-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fab07-117">-Name</span></span>
<span data-ttu-id="fab07-118">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fab07-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab07-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fab07-119">-PassThru</span></span>
<span data-ttu-id="fab07-120">Meghatározza, hogy visszaadja-e az eltávolított szinkronizálási csoportot</span><span class="sxs-lookup"><span data-stu-id="fab07-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="fab07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab07-121">-ResourceGroupName</span></span>
<span data-ttu-id="fab07-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fab07-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fab07-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fab07-123">-ServerName</span></span>
<span data-ttu-id="fab07-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="fab07-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fab07-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fab07-125">-Confirm</span></span>
<span data-ttu-id="fab07-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fab07-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab07-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab07-127">-WhatIf</span></span>
<span data-ttu-id="fab07-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fab07-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab07-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fab07-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab07-130">CommonParameters</span></span>
<span data-ttu-id="fab07-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab07-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fab07-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab07-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fab07-133">INPUTS</span></span>

### <span data-ttu-id="fab07-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fab07-134">System.String</span></span>

## <span data-ttu-id="fab07-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fab07-135">OUTPUTS</span></span>

### <span data-ttu-id="fab07-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="fab07-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="fab07-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fab07-137">NOTES</span></span>

## <span data-ttu-id="fab07-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fab07-138">RELATED LINKS</span></span>

[<span data-ttu-id="fab07-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fab07-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="fab07-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fab07-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="fab07-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fab07-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

