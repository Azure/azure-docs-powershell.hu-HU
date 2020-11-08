---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186652"
---
# <span data-ttu-id="2e340-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2e340-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="2e340-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e340-102">SYNOPSIS</span></span>
<span data-ttu-id="2e340-103">Azure SQL-szinkronizáló ügynök kulcs létrehozása.</span><span class="sxs-lookup"><span data-stu-id="2e340-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="2e340-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e340-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e340-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e340-105">DESCRIPTION</span></span>
<span data-ttu-id="2e340-106">A **New-AzSqlSyncAgentKey** parancsmag az Azure SQL Sync Agent kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2e340-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2e340-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e340-107">EXAMPLES</span></span>

### <span data-ttu-id="2e340-108">1. példa: a Szinkronizáló ügynök kulcsa az Azure SQL szinkronizáló ügynök számára.</span><span class="sxs-lookup"><span data-stu-id="2e340-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2e340-109">Ez a parancs létrehoz egy szinkronizáló ügynököt egy Azure SQL szinkronizáló ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="2e340-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2e340-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e340-110">PARAMETERS</span></span>

### <span data-ttu-id="2e340-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e340-111">-DefaultProfile</span></span>
<span data-ttu-id="2e340-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2e340-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e340-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e340-113">-ResourceGroupName</span></span>
<span data-ttu-id="2e340-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e340-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e340-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2e340-115">-ServerName</span></span>
<span data-ttu-id="2e340-116">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="2e340-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2e340-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2e340-117">-SyncAgentName</span></span>
<span data-ttu-id="2e340-118">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="2e340-118">The sync agent name.</span></span>

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

### <span data-ttu-id="2e340-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e340-119">-Confirm</span></span>
<span data-ttu-id="2e340-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e340-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e340-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e340-121">-WhatIf</span></span>
<span data-ttu-id="2e340-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e340-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e340-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e340-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e340-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e340-124">CommonParameters</span></span>
<span data-ttu-id="2e340-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e340-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e340-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e340-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e340-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e340-127">INPUTS</span></span>

### <span data-ttu-id="2e340-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2e340-128">System.String</span></span>

## <span data-ttu-id="2e340-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e340-129">OUTPUTS</span></span>

### <span data-ttu-id="2e340-130">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="2e340-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2e340-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e340-131">NOTES</span></span>

## <span data-ttu-id="2e340-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e340-132">RELATED LINKS</span></span>
