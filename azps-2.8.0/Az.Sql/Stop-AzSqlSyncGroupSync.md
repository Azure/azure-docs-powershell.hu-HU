---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: e7c6dc8adc9aa3e5880b72997389144d0c402d89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839580"
---
# <span data-ttu-id="5fcf5-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="5fcf5-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="5fcf5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcf5-103">Szinkronizálási csoport szinkronizálásának leállítása</span><span class="sxs-lookup"><span data-stu-id="5fcf5-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="5fcf5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fcf5-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fcf5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fcf5-105">DESCRIPTION</span></span>
<span data-ttu-id="5fcf5-106">A **stop-AzSqlSyncGroupSync** parancsmag leállítja a szinkronizálási csoportok szinkronizálását.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="5fcf5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5fcf5-107">EXAMPLES</span></span>

### <span data-ttu-id="5fcf5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5fcf5-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="5fcf5-109">Ez a parancs leállítja a szinkronizálás csoport mysg zajló szinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="5fcf5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fcf5-110">PARAMETERS</span></span>

### <span data-ttu-id="5fcf5-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5fcf5-111">-DatabaseName</span></span>
<span data-ttu-id="5fcf5-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5fcf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcf5-113">-DefaultProfile</span></span>
<span data-ttu-id="5fcf5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5fcf5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fcf5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fcf5-115">-PassThru</span></span>
<span data-ttu-id="5fcf5-116">Azt határozza meg, hogy a szinkronizálási csoportot adja-e vissza</span><span class="sxs-lookup"><span data-stu-id="5fcf5-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="5fcf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fcf5-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5fcf5-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5fcf5-119">-ServerName</span></span>
<span data-ttu-id="5fcf5-120">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5fcf5-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcf5-121">-SyncGroupName</span></span>
<span data-ttu-id="5fcf5-122">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-122">The sync group name.</span></span>

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

### <span data-ttu-id="5fcf5-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fcf5-123">-Confirm</span></span>
<span data-ttu-id="5fcf5-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fcf5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fcf5-125">-WhatIf</span></span>
<span data-ttu-id="5fcf5-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fcf5-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fcf5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcf5-128">CommonParameters</span></span>
<span data-ttu-id="5fcf5-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fcf5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcf5-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5fcf5-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcf5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fcf5-131">INPUTS</span></span>

### <span data-ttu-id="5fcf5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5fcf5-132">System.String</span></span>

## <span data-ttu-id="5fcf5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fcf5-133">OUTPUTS</span></span>

### <span data-ttu-id="5fcf5-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5fcf5-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5fcf5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fcf5-135">NOTES</span></span>

## <span data-ttu-id="5fcf5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fcf5-136">RELATED LINKS</span></span>

[<span data-ttu-id="5fcf5-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="5fcf5-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

