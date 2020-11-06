---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 9886d2d32dd3bce8841dcf2652cf89054335b112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502843"
---
# <span data-ttu-id="caf11-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="caf11-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="caf11-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="caf11-102">SYNOPSIS</span></span>
<span data-ttu-id="caf11-103">Azure SQL-szinkronizálási ügynök eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="caf11-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf11-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="caf11-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caf11-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="caf11-105">DESCRIPTION</span></span>
<span data-ttu-id="caf11-106">A **Remove-AzureRmSqlSyncAgent** parancsmag eltávolítja az Azure SQL szinkronizáló ügynököt.</span><span class="sxs-lookup"><span data-stu-id="caf11-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="caf11-107">Példák</span><span class="sxs-lookup"><span data-stu-id="caf11-107">EXAMPLES</span></span>

### <span data-ttu-id="caf11-108">1. példa: a Szinkronizáló ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="caf11-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="caf11-109">Ez a parancs eltávolítja a syncAgent01 nevű Azure SQL-szinkronizáló ügynököt.</span><span class="sxs-lookup"><span data-stu-id="caf11-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="caf11-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="caf11-110">PARAMETERS</span></span>

### <span data-ttu-id="caf11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf11-111">-DefaultProfile</span></span>
<span data-ttu-id="caf11-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="caf11-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caf11-113">-Force</span><span class="sxs-lookup"><span data-stu-id="caf11-113">-Force</span></span>
<span data-ttu-id="caf11-114">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="caf11-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="caf11-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="caf11-115">-Name</span></span>
<span data-ttu-id="caf11-116">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="caf11-116">The sync agent name.</span></span>

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

### <span data-ttu-id="caf11-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caf11-117">-PassThru</span></span>
<span data-ttu-id="caf11-118">Annak meghatározása, hogy az eltávolított szinkronizáló ügynök visszaadja-e</span><span class="sxs-lookup"><span data-stu-id="caf11-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="caf11-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf11-119">-ResourceGroupName</span></span>
<span data-ttu-id="caf11-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="caf11-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="caf11-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="caf11-121">-ServerName</span></span>
<span data-ttu-id="caf11-122">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="caf11-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="caf11-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="caf11-123">-Confirm</span></span>
<span data-ttu-id="caf11-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="caf11-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caf11-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf11-125">-WhatIf</span></span>
<span data-ttu-id="caf11-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="caf11-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caf11-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="caf11-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caf11-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf11-128">CommonParameters</span></span>
<span data-ttu-id="caf11-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="caf11-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf11-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf11-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf11-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="caf11-131">INPUTS</span></span>

### <span data-ttu-id="caf11-132">System. String</span><span class="sxs-lookup"><span data-stu-id="caf11-132">System.String</span></span>

## <span data-ttu-id="caf11-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caf11-133">OUTPUTS</span></span>

### <span data-ttu-id="caf11-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="caf11-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="caf11-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="caf11-135">NOTES</span></span>

## <span data-ttu-id="caf11-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caf11-136">RELATED LINKS</span></span>

[<span data-ttu-id="caf11-137">Új – AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="caf11-137">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="caf11-138">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="caf11-138">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

