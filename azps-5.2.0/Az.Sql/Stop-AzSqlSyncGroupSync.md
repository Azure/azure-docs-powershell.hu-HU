---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330473"
---
# <span data-ttu-id="b6bcb-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="b6bcb-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="b6bcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bcb-103">Leállítja a szinkronizálási csoport szinkronizálását.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="b6bcb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6bcb-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6bcb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6bcb-105">DESCRIPTION</span></span>
<span data-ttu-id="b6bcb-106">A **Stop-AzSqlSyncGroupSync** parancsmag leállítja a szinkronizálási csoport szinkronizálását.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="b6bcb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6bcb-107">EXAMPLES</span></span>

### <span data-ttu-id="b6bcb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b6bcb-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="b6bcb-109">Ez a parancs leállítja a szinkronizálást, amely folyamatban van a sajátsg szinkronizálási csoportban.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="b6bcb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6bcb-110">PARAMETERS</span></span>

### <span data-ttu-id="b6bcb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b6bcb-111">-DatabaseName</span></span>
<span data-ttu-id="b6bcb-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b6bcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bcb-113">-DefaultProfile</span></span>
<span data-ttu-id="b6bcb-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b6bcb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6bcb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6bcb-115">-PassThru</span></span>
<span data-ttu-id="b6bcb-116">Meghatározza, hogy visszaadja-e a szinkronizálási csoportot</span><span class="sxs-lookup"><span data-stu-id="b6bcb-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="b6bcb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bcb-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6bcb-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6bcb-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6bcb-119">-ServerName</span></span>
<span data-ttu-id="b6bcb-120">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b6bcb-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bcb-121">-SyncGroupName</span></span>
<span data-ttu-id="b6bcb-122">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bcb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6bcb-123">-Confirm</span></span>
<span data-ttu-id="b6bcb-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6bcb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6bcb-125">-WhatIf</span></span>
<span data-ttu-id="b6bcb-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6bcb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6bcb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bcb-128">CommonParameters</span></span>
<span data-ttu-id="b6bcb-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bcb-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6bcb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bcb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6bcb-131">INPUTS</span></span>

### <span data-ttu-id="b6bcb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b6bcb-132">System.String</span></span>

## <span data-ttu-id="b6bcb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6bcb-133">OUTPUTS</span></span>

### <span data-ttu-id="b6bcb-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="b6bcb-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="b6bcb-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6bcb-135">NOTES</span></span>

## <span data-ttu-id="b6bcb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6bcb-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6bcb-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="b6bcb-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

