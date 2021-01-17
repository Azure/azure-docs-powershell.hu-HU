---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466015"
---
# <span data-ttu-id="bd2b1-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="bd2b1-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="bd2b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2b1-103">Eltávolít egy Azure SQL Sync-ügynököt.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="bd2b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd2b1-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd2b1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd2b1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd2b1-106">A **Remove-AzSqlSyncAgent** parancsmag eltávolítja az Azure SQL Sync-ügynökét.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="bd2b1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd2b1-107">EXAMPLES</span></span>

### <span data-ttu-id="bd2b1-108">1. példa: Szinkronizálási ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bd2b1-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="bd2b1-109">Ez a parancs eltávolítja a syncAgent01 nevű Azure SQL Sync Agentt.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="bd2b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd2b1-110">PARAMETERS</span></span>

### <span data-ttu-id="bd2b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2b1-111">-DefaultProfile</span></span>
<span data-ttu-id="bd2b1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bd2b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd2b1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bd2b1-113">-Force</span></span>
<span data-ttu-id="bd2b1-114">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="bd2b1-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bd2b1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bd2b1-115">-Name</span></span>
<span data-ttu-id="bd2b1-116">A szinkronizálási ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2b1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd2b1-117">-PassThru</span></span>
<span data-ttu-id="bd2b1-118">Meghatározza, hogy visszaadja-e az eltávolított szinkronizálási ügynök</span><span class="sxs-lookup"><span data-stu-id="bd2b1-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="bd2b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd2b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd2b1-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd2b1-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd2b1-121">-ServerName</span></span>
<span data-ttu-id="bd2b1-122">Annak az Azure SQL Servernek a neve, amelyben a szinkronizálási ügynök található.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="bd2b1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd2b1-123">-Confirm</span></span>
<span data-ttu-id="bd2b1-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd2b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd2b1-125">-WhatIf</span></span>
<span data-ttu-id="bd2b1-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd2b1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd2b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2b1-128">CommonParameters</span></span>
<span data-ttu-id="bd2b1-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd2b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2b1-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd2b1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2b1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd2b1-131">INPUTS</span></span>

### <span data-ttu-id="bd2b1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bd2b1-132">System.String</span></span>

## <span data-ttu-id="bd2b1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd2b1-133">OUTPUTS</span></span>

### <span data-ttu-id="bd2b1-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="bd2b1-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="bd2b1-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd2b1-135">NOTES</span></span>

## <span data-ttu-id="bd2b1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd2b1-136">RELATED LINKS</span></span>

[<span data-ttu-id="bd2b1-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="bd2b1-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="bd2b1-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="bd2b1-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

