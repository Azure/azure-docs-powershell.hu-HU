---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 481f99baa432c00fc6a619754cee2df83015c047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672268"
---
# <span data-ttu-id="c502f-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c502f-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="c502f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c502f-102">SYNOPSIS</span></span>
<span data-ttu-id="c502f-103">Azure SQL-szinkronizálási ügynök eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c502f-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c502f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c502f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c502f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c502f-105">DESCRIPTION</span></span>
<span data-ttu-id="c502f-106">A **Remove-AzureRmSqlSyncAgent** parancsmag eltávolítja az Azure SQL szinkronizáló ügynököt.</span><span class="sxs-lookup"><span data-stu-id="c502f-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="c502f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c502f-107">EXAMPLES</span></span>

### <span data-ttu-id="c502f-108">1. példa: a Szinkronizáló ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c502f-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="c502f-109">Ez a parancs eltávolítja a syncAgent01 nevű Azure SQL-szinkronizáló ügynököt.</span><span class="sxs-lookup"><span data-stu-id="c502f-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="c502f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c502f-110">PARAMETERS</span></span>

### <span data-ttu-id="c502f-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c502f-111">-Confirm</span></span>
<span data-ttu-id="c502f-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c502f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c502f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c502f-113">-Force</span></span>
<span data-ttu-id="c502f-114">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="c502f-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c502f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c502f-115">-Name</span></span>
<span data-ttu-id="c502f-116">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="c502f-116">The sync agent name.</span></span>

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

### <span data-ttu-id="c502f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c502f-117">-PassThru</span></span>
<span data-ttu-id="c502f-118">Annak meghatározása, hogy az eltávolított szinkronizáló ügynök visszaadja-e</span><span class="sxs-lookup"><span data-stu-id="c502f-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="c502f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c502f-119">-ResourceGroupName</span></span>
<span data-ttu-id="c502f-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c502f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c502f-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c502f-121">-ServerName</span></span>
<span data-ttu-id="c502f-122">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="c502f-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="c502f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c502f-123">-WhatIf</span></span>
<span data-ttu-id="c502f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c502f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c502f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c502f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c502f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c502f-126">-DefaultProfile</span></span>
<span data-ttu-id="c502f-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c502f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c502f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c502f-128">CommonParameters</span></span>
<span data-ttu-id="c502f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c502f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c502f-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c502f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c502f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c502f-131">INPUTS</span></span>

## <span data-ttu-id="c502f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c502f-132">OUTPUTS</span></span>

### <span data-ttu-id="c502f-133">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="c502f-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="c502f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c502f-134">NOTES</span></span>

## <span data-ttu-id="c502f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c502f-135">RELATED LINKS</span></span>

[<span data-ttu-id="c502f-136">Új – AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c502f-136">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="c502f-137">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c502f-137">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

