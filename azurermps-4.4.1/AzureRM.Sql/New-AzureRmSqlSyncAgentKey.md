---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: 254f2def5a1be57840ea195f326534ce883870df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496812"
---
# <span data-ttu-id="f056c-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="f056c-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="f056c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f056c-102">SYNOPSIS</span></span>
<span data-ttu-id="f056c-103">Azure SQL-szinkronizáló ügynök kulcs létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f056c-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f056c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f056c-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f056c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f056c-105">DESCRIPTION</span></span>
<span data-ttu-id="f056c-106">A **New-AzureRmSqlSyncAgentKey** parancsmag az Azure SQL Sync Agent kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f056c-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="f056c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f056c-107">EXAMPLES</span></span>

### <span data-ttu-id="f056c-108">1. példa: a Szinkronizáló ügynök kulcsa az Azure SQL szinkronizáló ügynök számára.</span><span class="sxs-lookup"><span data-stu-id="f056c-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="f056c-109">Ez a parancs létrehoz egy szinkronizáló ügynököt egy Azure SQL szinkronizáló ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="f056c-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="f056c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f056c-110">PARAMETERS</span></span>

### <span data-ttu-id="f056c-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f056c-111">-Confirm</span></span>
<span data-ttu-id="f056c-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f056c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f056c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f056c-113">-ResourceGroupName</span></span>
<span data-ttu-id="f056c-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f056c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="f056c-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f056c-115">-ServerName</span></span>
<span data-ttu-id="f056c-116">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="f056c-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f056c-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="f056c-117">-SyncAgentName</span></span>
<span data-ttu-id="f056c-118">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="f056c-118">The sync agent name.</span></span>

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

### <span data-ttu-id="f056c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f056c-119">-WhatIf</span></span>
<span data-ttu-id="f056c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f056c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f056c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f056c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f056c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f056c-122">-DefaultProfile</span></span>
<span data-ttu-id="f056c-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f056c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f056c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f056c-124">CommonParameters</span></span>
<span data-ttu-id="f056c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f056c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f056c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f056c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f056c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f056c-127">INPUTS</span></span>

## <span data-ttu-id="f056c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f056c-128">OUTPUTS</span></span>

### <span data-ttu-id="f056c-129">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="f056c-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="f056c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f056c-130">NOTES</span></span>

## <span data-ttu-id="f056c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f056c-131">RELATED LINKS</span></span>

