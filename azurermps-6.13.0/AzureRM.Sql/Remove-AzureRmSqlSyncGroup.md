---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 62f3c74f94ac0e775adc70f4eef9c4250e041145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504268"
---
# <span data-ttu-id="19f2c-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19f2c-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="19f2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="19f2c-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="19f2c-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19f2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19f2c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19f2c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19f2c-105">DESCRIPTION</span></span>
<span data-ttu-id="19f2c-106">A **Remove-AzureRmSqlSyncGroup** parancsmag eltávolítja az Azure SQL-adatbázis szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="19f2c-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="19f2c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19f2c-107">EXAMPLES</span></span>

### <span data-ttu-id="19f2c-108">1. példa: szinkronizálási csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="19f2c-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="19f2c-109">Ez a parancs eltávolítja a syncGroup01 nevű Azure SQL-adatbázis szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="19f2c-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="19f2c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19f2c-110">PARAMETERS</span></span>

### <span data-ttu-id="19f2c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19f2c-111">-DatabaseName</span></span>
<span data-ttu-id="19f2c-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="19f2c-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="19f2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f2c-113">-DefaultProfile</span></span>
<span data-ttu-id="19f2c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19f2c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19f2c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="19f2c-115">-Force</span></span>
<span data-ttu-id="19f2c-116">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="19f2c-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="19f2c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19f2c-117">-Name</span></span>
<span data-ttu-id="19f2c-118">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="19f2c-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19f2c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19f2c-119">-PassThru</span></span>
<span data-ttu-id="19f2c-120">Annak meghatározása, hogy az eltávolított szinkronizálási csoportot adja vissza</span><span class="sxs-lookup"><span data-stu-id="19f2c-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="19f2c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f2c-121">-ResourceGroupName</span></span>
<span data-ttu-id="19f2c-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="19f2c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="19f2c-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="19f2c-123">-ServerName</span></span>
<span data-ttu-id="19f2c-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="19f2c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="19f2c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19f2c-125">-Confirm</span></span>
<span data-ttu-id="19f2c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19f2c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f2c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f2c-127">-WhatIf</span></span>
<span data-ttu-id="19f2c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19f2c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19f2c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19f2c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f2c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f2c-130">CommonParameters</span></span>
<span data-ttu-id="19f2c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19f2c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f2c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f2c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f2c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19f2c-133">INPUTS</span></span>

### <span data-ttu-id="19f2c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="19f2c-134">System.String</span></span>

## <span data-ttu-id="19f2c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19f2c-135">OUTPUTS</span></span>

### <span data-ttu-id="19f2c-136">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="19f2c-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="19f2c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19f2c-137">NOTES</span></span>

## <span data-ttu-id="19f2c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19f2c-138">RELATED LINKS</span></span>

[<span data-ttu-id="19f2c-139">Új – AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19f2c-139">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="19f2c-140">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19f2c-140">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="19f2c-141">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19f2c-141">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)
