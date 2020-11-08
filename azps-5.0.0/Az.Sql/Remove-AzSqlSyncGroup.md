---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186977"
---
# <span data-ttu-id="96be7-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96be7-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="96be7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96be7-102">SYNOPSIS</span></span>
<span data-ttu-id="96be7-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="96be7-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="96be7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96be7-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96be7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96be7-105">DESCRIPTION</span></span>
<span data-ttu-id="96be7-106">A **Remove-AzSqlSyncGroup** parancsmag eltávolítja az Azure SQL-adatbázis szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="96be7-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="96be7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96be7-107">EXAMPLES</span></span>

### <span data-ttu-id="96be7-108">1. példa: szinkronizálási csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="96be7-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="96be7-109">Ez a parancs eltávolítja a syncGroup01 nevű Azure SQL-adatbázis szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="96be7-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="96be7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96be7-110">PARAMETERS</span></span>

### <span data-ttu-id="96be7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96be7-111">-DatabaseName</span></span>
<span data-ttu-id="96be7-112">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="96be7-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="96be7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96be7-113">-DefaultProfile</span></span>
<span data-ttu-id="96be7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="96be7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96be7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="96be7-115">-Force</span></span>
<span data-ttu-id="96be7-116">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="96be7-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="96be7-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96be7-117">-Name</span></span>
<span data-ttu-id="96be7-118">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="96be7-118">The sync group name.</span></span>

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

### <span data-ttu-id="96be7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96be7-119">-PassThru</span></span>
<span data-ttu-id="96be7-120">Annak meghatározása, hogy az eltávolított szinkronizálási csoportot adja vissza</span><span class="sxs-lookup"><span data-stu-id="96be7-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="96be7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96be7-121">-ResourceGroupName</span></span>
<span data-ttu-id="96be7-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="96be7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="96be7-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="96be7-123">-ServerName</span></span>
<span data-ttu-id="96be7-124">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="96be7-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="96be7-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96be7-125">-Confirm</span></span>
<span data-ttu-id="96be7-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96be7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96be7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96be7-127">-WhatIf</span></span>
<span data-ttu-id="96be7-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96be7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96be7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96be7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96be7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96be7-130">CommonParameters</span></span>
<span data-ttu-id="96be7-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96be7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96be7-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96be7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96be7-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96be7-133">INPUTS</span></span>

### <span data-ttu-id="96be7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="96be7-134">System.String</span></span>

## <span data-ttu-id="96be7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96be7-135">OUTPUTS</span></span>

### <span data-ttu-id="96be7-136">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="96be7-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="96be7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96be7-137">NOTES</span></span>

## <span data-ttu-id="96be7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96be7-138">RELATED LINKS</span></span>

[<span data-ttu-id="96be7-139">Új – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96be7-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="96be7-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96be7-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="96be7-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96be7-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

