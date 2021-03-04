---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 35942c51aa383dbc7dcbe071083eee575228372a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921610"
---
# <span data-ttu-id="482c8-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="482c8-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="482c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="482c8-102">SYNOPSIS</span></span>
<span data-ttu-id="482c8-103">Létrehoz egy Azure SQL Sync ügynökkulcsot.</span><span class="sxs-lookup"><span data-stu-id="482c8-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="482c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="482c8-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="482c8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="482c8-105">DESCRIPTION</span></span>
<span data-ttu-id="482c8-106">A **New-AzSqlSyncAgentKey** parancsmag létrehoz egy Azure SQL Sync Agent kulcsot.</span><span class="sxs-lookup"><span data-stu-id="482c8-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="482c8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="482c8-107">EXAMPLES</span></span>

### <span data-ttu-id="482c8-108">1. példa: Szinkronizálási ügynökkulcs létrehozása egy Azure SQL-szinkronizálási ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="482c8-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="482c8-109">Ez a parancs szinkronizálási ügynökkulcsot hoz létre egy Azure SQL Sync-ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="482c8-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="482c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="482c8-110">PARAMETERS</span></span>

### <span data-ttu-id="482c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482c8-111">-DefaultProfile</span></span>
<span data-ttu-id="482c8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="482c8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="482c8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="482c8-113">-ResourceGroupName</span></span>
<span data-ttu-id="482c8-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="482c8-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="482c8-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="482c8-115">-ServerName</span></span>
<span data-ttu-id="482c8-116">Annak az Azure SQL Servernek a neve, amelyben a szinkronizálási ügynök található.</span><span class="sxs-lookup"><span data-stu-id="482c8-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="482c8-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="482c8-117">-SyncAgentName</span></span>
<span data-ttu-id="482c8-118">A szinkronizálási ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="482c8-118">The sync agent name.</span></span>

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

### <span data-ttu-id="482c8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="482c8-119">-Confirm</span></span>
<span data-ttu-id="482c8-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="482c8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="482c8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="482c8-121">-WhatIf</span></span>
<span data-ttu-id="482c8-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="482c8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="482c8-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="482c8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="482c8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482c8-124">CommonParameters</span></span>
<span data-ttu-id="482c8-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="482c8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482c8-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="482c8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482c8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="482c8-127">INPUTS</span></span>

### <span data-ttu-id="482c8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="482c8-128">System.String</span></span>

## <span data-ttu-id="482c8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="482c8-129">OUTPUTS</span></span>

### <span data-ttu-id="482c8-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="482c8-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="482c8-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="482c8-131">NOTES</span></span>

## <span data-ttu-id="482c8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="482c8-132">RELATED LINKS</span></span>
