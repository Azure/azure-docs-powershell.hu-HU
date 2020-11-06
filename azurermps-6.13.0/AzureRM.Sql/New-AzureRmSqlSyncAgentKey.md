---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: cb4ca947d9f87cd6a0d3b4cdf476cf0176db2c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492705"
---
# <span data-ttu-id="11f7d-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="11f7d-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="11f7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="11f7d-103">Azure SQL-szinkronizáló ügynök kulcs létrehozása.</span><span class="sxs-lookup"><span data-stu-id="11f7d-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11f7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11f7d-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11f7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="11f7d-106">A **New-AzureRmSqlSyncAgentKey** parancsmag az Azure SQL Sync Agent kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="11f7d-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="11f7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="11f7d-108">1. példa: a Szinkronizáló ügynök kulcsa az Azure SQL szinkronizáló ügynök számára.</span><span class="sxs-lookup"><span data-stu-id="11f7d-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="11f7d-109">Ez a parancs létrehoz egy szinkronizáló ügynököt egy Azure SQL szinkronizáló ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="11f7d-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="11f7d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11f7d-110">PARAMETERS</span></span>

### <span data-ttu-id="11f7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f7d-111">-DefaultProfile</span></span>
<span data-ttu-id="11f7d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11f7d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11f7d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f7d-113">-ResourceGroupName</span></span>
<span data-ttu-id="11f7d-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11f7d-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="11f7d-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="11f7d-115">-ServerName</span></span>
<span data-ttu-id="11f7d-116">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="11f7d-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="11f7d-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="11f7d-117">-SyncAgentName</span></span>
<span data-ttu-id="11f7d-118">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="11f7d-118">The sync agent name.</span></span>

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

### <span data-ttu-id="11f7d-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11f7d-119">-Confirm</span></span>
<span data-ttu-id="11f7d-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11f7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11f7d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f7d-121">-WhatIf</span></span>
<span data-ttu-id="11f7d-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11f7d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11f7d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11f7d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11f7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f7d-124">CommonParameters</span></span>
<span data-ttu-id="11f7d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11f7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f7d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f7d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f7d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11f7d-127">INPUTS</span></span>

### <span data-ttu-id="11f7d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="11f7d-128">System.String</span></span>

## <span data-ttu-id="11f7d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11f7d-129">OUTPUTS</span></span>

### <span data-ttu-id="11f7d-130">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="11f7d-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="11f7d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11f7d-131">NOTES</span></span>

## <span data-ttu-id="11f7d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11f7d-132">RELATED LINKS</span></span>
