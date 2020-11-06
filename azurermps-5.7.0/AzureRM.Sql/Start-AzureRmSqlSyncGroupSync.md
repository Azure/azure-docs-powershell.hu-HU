---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 040b08e328cb06629e706350fa14752fa6918954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495225"
---
# <span data-ttu-id="a6dc7-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a6dc7-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="a6dc7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="a6dc7-103">Szinkronizálási csoport szinkronizálását indítja el.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6dc7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6dc7-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6dc7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="a6dc7-106">A **Start-AzureRmSqlSyncGroupSync** parancsmag szinkronizálási csoport szinkronizálását indítja el.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="a6dc7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a6dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="a6dc7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a6dc7-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="a6dc7-109">Ez a parancs elindítja a szinkronizálást a szinkronizálás csoport mysg.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="a6dc7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6dc7-110">PARAMETERS</span></span>

### <span data-ttu-id="a6dc7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a6dc7-111">-DatabaseName</span></span>
<span data-ttu-id="a6dc7-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6dc7-113">-DefaultProfile</span></span>
<span data-ttu-id="a6dc7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a6dc7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6dc7-115">-PassThru</span></span>
<span data-ttu-id="a6dc7-116">Azt határozza meg, hogy a szinkronizálási csoportot adja-e vissza</span><span class="sxs-lookup"><span data-stu-id="a6dc7-116">Defines Whether return the sync group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6dc7-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6dc7-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a6dc7-119">-ServerName</span></span>
<span data-ttu-id="a6dc7-120">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-120">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a6dc7-121">-SyncGroupName</span></span>
<span data-ttu-id="a6dc7-122">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6dc7-123">-Confirm</span></span>
<span data-ttu-id="a6dc7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6dc7-125">-WhatIf</span></span>
<span data-ttu-id="a6dc7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6dc7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6dc7-128">CommonParameters</span></span>
<span data-ttu-id="a6dc7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6dc7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6dc7-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6dc7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6dc7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6dc7-131">INPUTS</span></span>

### <span data-ttu-id="a6dc7-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="a6dc7-132">None</span></span>
<span data-ttu-id="a6dc7-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6dc7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6dc7-134">OUTPUTS</span></span>

### <span data-ttu-id="a6dc7-135">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a6dc7-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a6dc7-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6dc7-136">NOTES</span></span>

## <span data-ttu-id="a6dc7-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6dc7-137">RELATED LINKS</span></span>

[<span data-ttu-id="a6dc7-138">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a6dc7-138">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

