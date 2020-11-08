---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183900"
---
# <span data-ttu-id="ecd57-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="ecd57-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="ecd57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ecd57-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd57-103">Azure SQL-szinkronizálási ügynök eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ecd57-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="ecd57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ecd57-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ecd57-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd57-106">A **Remove-AzSqlSyncAgent** parancsmag eltávolítja az Azure SQL szinkronizáló ügynököt.</span><span class="sxs-lookup"><span data-stu-id="ecd57-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="ecd57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ecd57-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd57-108">1. példa: a Szinkronizáló ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ecd57-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="ecd57-109">Ez a parancs eltávolítja a syncAgent01 nevű Azure SQL-szinkronizáló ügynököt.</span><span class="sxs-lookup"><span data-stu-id="ecd57-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="ecd57-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ecd57-110">PARAMETERS</span></span>

### <span data-ttu-id="ecd57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd57-111">-DefaultProfile</span></span>
<span data-ttu-id="ecd57-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ecd57-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecd57-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ecd57-113">-Force</span></span>
<span data-ttu-id="ecd57-114">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="ecd57-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ecd57-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ecd57-115">-Name</span></span>
<span data-ttu-id="ecd57-116">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="ecd57-116">The sync agent name.</span></span>

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

### <span data-ttu-id="ecd57-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecd57-117">-PassThru</span></span>
<span data-ttu-id="ecd57-118">Annak meghatározása, hogy az eltávolított szinkronizáló ügynök visszaadja-e</span><span class="sxs-lookup"><span data-stu-id="ecd57-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="ecd57-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd57-119">-ResourceGroupName</span></span>
<span data-ttu-id="ecd57-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ecd57-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecd57-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ecd57-121">-ServerName</span></span>
<span data-ttu-id="ecd57-122">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="ecd57-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="ecd57-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ecd57-123">-Confirm</span></span>
<span data-ttu-id="ecd57-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecd57-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd57-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd57-125">-WhatIf</span></span>
<span data-ttu-id="ecd57-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ecd57-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd57-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecd57-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd57-128">CommonParameters</span></span>
<span data-ttu-id="ecd57-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ecd57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd57-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ecd57-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd57-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecd57-131">INPUTS</span></span>

### <span data-ttu-id="ecd57-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd57-132">System.String</span></span>

## <span data-ttu-id="ecd57-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecd57-133">OUTPUTS</span></span>

### <span data-ttu-id="ecd57-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="ecd57-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="ecd57-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ecd57-135">NOTES</span></span>

## <span data-ttu-id="ecd57-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecd57-136">RELATED LINKS</span></span>

[<span data-ttu-id="ecd57-137">Új – AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="ecd57-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="ecd57-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="ecd57-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

