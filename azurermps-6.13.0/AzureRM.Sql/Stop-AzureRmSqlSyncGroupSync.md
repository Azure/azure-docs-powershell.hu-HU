---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 9cd213aea4e6211f52b076fca753385aefb1b449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494854"
---
# <span data-ttu-id="929e0-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="929e0-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="929e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="929e0-102">SYNOPSIS</span></span>
<span data-ttu-id="929e0-103">Szinkronizálási csoport szinkronizálásának leállítása</span><span class="sxs-lookup"><span data-stu-id="929e0-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="929e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="929e0-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="929e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="929e0-105">DESCRIPTION</span></span>
<span data-ttu-id="929e0-106">A **stop-AzureRmSqlSyncGroupSync** parancsmag leállítja a szinkronizálási csoportok szinkronizálását.</span><span class="sxs-lookup"><span data-stu-id="929e0-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="929e0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="929e0-107">EXAMPLES</span></span>

### <span data-ttu-id="929e0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="929e0-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="929e0-109">Ez a parancs leállítja a szinkronizálás csoport mysg zajló szinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="929e0-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="929e0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="929e0-110">PARAMETERS</span></span>

### <span data-ttu-id="929e0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="929e0-111">-DatabaseName</span></span>
<span data-ttu-id="929e0-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="929e0-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="929e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929e0-113">-DefaultProfile</span></span>
<span data-ttu-id="929e0-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="929e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="929e0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="929e0-115">-PassThru</span></span>
<span data-ttu-id="929e0-116">Azt határozza meg, hogy a szinkronizálási csoportot adja-e vissza</span><span class="sxs-lookup"><span data-stu-id="929e0-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="929e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="929e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="929e0-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="929e0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="929e0-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="929e0-119">-ServerName</span></span>
<span data-ttu-id="929e0-120">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="929e0-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="929e0-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="929e0-121">-SyncGroupName</span></span>
<span data-ttu-id="929e0-122">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="929e0-122">The sync group name.</span></span>

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

### <span data-ttu-id="929e0-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="929e0-123">-Confirm</span></span>
<span data-ttu-id="929e0-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="929e0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="929e0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="929e0-125">-WhatIf</span></span>
<span data-ttu-id="929e0-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="929e0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="929e0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="929e0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="929e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929e0-128">CommonParameters</span></span>
<span data-ttu-id="929e0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="929e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929e0-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="929e0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929e0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="929e0-131">INPUTS</span></span>

### <span data-ttu-id="929e0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="929e0-132">System.String</span></span>

## <span data-ttu-id="929e0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="929e0-133">OUTPUTS</span></span>

### <span data-ttu-id="929e0-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="929e0-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="929e0-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="929e0-135">NOTES</span></span>

## <span data-ttu-id="929e0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="929e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="929e0-137">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="929e0-137">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

