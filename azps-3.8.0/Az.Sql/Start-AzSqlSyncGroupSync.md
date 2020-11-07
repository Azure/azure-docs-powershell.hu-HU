---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846518"
---
# <span data-ttu-id="0fee3-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="0fee3-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="0fee3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fee3-102">SYNOPSIS</span></span>
<span data-ttu-id="0fee3-103">Szinkronizálási csoport szinkronizálását indítja el.</span><span class="sxs-lookup"><span data-stu-id="0fee3-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="0fee3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fee3-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fee3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fee3-105">DESCRIPTION</span></span>
<span data-ttu-id="0fee3-106">A **Start-AzSqlSyncGroupSync** parancsmag szinkronizálási csoport szinkronizálását indítja el.</span><span class="sxs-lookup"><span data-stu-id="0fee3-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="0fee3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0fee3-107">EXAMPLES</span></span>

### <span data-ttu-id="0fee3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fee3-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="0fee3-109">Ez a parancs elindítja a szinkronizálást a szinkronizálás csoport mysg.</span><span class="sxs-lookup"><span data-stu-id="0fee3-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="0fee3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fee3-110">PARAMETERS</span></span>

### <span data-ttu-id="0fee3-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0fee3-111">-DatabaseName</span></span>
<span data-ttu-id="0fee3-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0fee3-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0fee3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fee3-113">-DefaultProfile</span></span>
<span data-ttu-id="0fee3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0fee3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fee3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fee3-115">-PassThru</span></span>
<span data-ttu-id="0fee3-116">Azt határozza meg, hogy a szinkronizálási csoportot adja-e vissza</span><span class="sxs-lookup"><span data-stu-id="0fee3-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="0fee3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fee3-117">-ResourceGroupName</span></span>
<span data-ttu-id="0fee3-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fee3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fee3-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0fee3-119">-ServerName</span></span>
<span data-ttu-id="0fee3-120">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="0fee3-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0fee3-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0fee3-121">-SyncGroupName</span></span>
<span data-ttu-id="0fee3-122">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fee3-122">The sync group name.</span></span>

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

### <span data-ttu-id="0fee3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fee3-123">-Confirm</span></span>
<span data-ttu-id="0fee3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fee3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fee3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fee3-125">-WhatIf</span></span>
<span data-ttu-id="0fee3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fee3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fee3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fee3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fee3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fee3-128">CommonParameters</span></span>
<span data-ttu-id="0fee3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fee3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fee3-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fee3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fee3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fee3-131">INPUTS</span></span>

### <span data-ttu-id="0fee3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0fee3-132">System.String</span></span>

## <span data-ttu-id="0fee3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fee3-133">OUTPUTS</span></span>

### <span data-ttu-id="0fee3-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="0fee3-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="0fee3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fee3-135">NOTES</span></span>

## <span data-ttu-id="0fee3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fee3-136">RELATED LINKS</span></span>

[<span data-ttu-id="0fee3-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="0fee3-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

