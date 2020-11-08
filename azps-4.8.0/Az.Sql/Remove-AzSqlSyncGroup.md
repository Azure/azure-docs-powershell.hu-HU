---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024343"
---
# <span data-ttu-id="b810a-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b810a-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="b810a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b810a-102">SYNOPSIS</span></span>
<span data-ttu-id="b810a-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b810a-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="b810a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b810a-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b810a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b810a-105">DESCRIPTION</span></span>
<span data-ttu-id="b810a-106">A **Remove-AzSqlSyncGroup** parancsmag eltávolítja az Azure SQL-adatbázis szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="b810a-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="b810a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b810a-107">EXAMPLES</span></span>

### <span data-ttu-id="b810a-108">1. példa: szinkronizálási csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b810a-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="b810a-109">Ez a parancs eltávolítja a syncGroup01 nevű Azure SQL-adatbázis szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="b810a-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="b810a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b810a-110">PARAMETERS</span></span>

### <span data-ttu-id="b810a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b810a-111">-DatabaseName</span></span>
<span data-ttu-id="b810a-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b810a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b810a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b810a-113">-DefaultProfile</span></span>
<span data-ttu-id="b810a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b810a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b810a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b810a-115">-Force</span></span>
<span data-ttu-id="b810a-116">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="b810a-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b810a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b810a-117">-Name</span></span>
<span data-ttu-id="b810a-118">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b810a-118">The sync group name.</span></span>

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

### <span data-ttu-id="b810a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b810a-119">-PassThru</span></span>
<span data-ttu-id="b810a-120">Annak meghatározása, hogy az eltávolított szinkronizálási csoportot adja vissza</span><span class="sxs-lookup"><span data-stu-id="b810a-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="b810a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b810a-121">-ResourceGroupName</span></span>
<span data-ttu-id="b810a-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b810a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b810a-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b810a-123">-ServerName</span></span>
<span data-ttu-id="b810a-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="b810a-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b810a-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b810a-125">-Confirm</span></span>
<span data-ttu-id="b810a-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b810a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b810a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b810a-127">-WhatIf</span></span>
<span data-ttu-id="b810a-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b810a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b810a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b810a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b810a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b810a-130">CommonParameters</span></span>
<span data-ttu-id="b810a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b810a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b810a-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b810a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b810a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b810a-133">INPUTS</span></span>

### <span data-ttu-id="b810a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b810a-134">System.String</span></span>

## <span data-ttu-id="b810a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b810a-135">OUTPUTS</span></span>

### <span data-ttu-id="b810a-136">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="b810a-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="b810a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b810a-137">NOTES</span></span>

## <span data-ttu-id="b810a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b810a-138">RELATED LINKS</span></span>

[<span data-ttu-id="b810a-139">Új – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b810a-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="b810a-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b810a-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="b810a-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b810a-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

