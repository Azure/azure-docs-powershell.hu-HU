---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 7022f8655e1b87bc55ddd90cbd0aca512eeec0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668753"
---
# <span data-ttu-id="65094-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="65094-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="65094-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65094-102">SYNOPSIS</span></span>
<span data-ttu-id="65094-103">Módosítja azt a kiszolgálót, amelyre az Azure SQL Server DNS-aliasa mutat</span><span class="sxs-lookup"><span data-stu-id="65094-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="65094-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65094-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65094-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65094-105">DESCRIPTION</span></span>
<span data-ttu-id="65094-106">Ez a parancs frissíti azt a kiszolgálót, amelyre az alias mutat.</span><span class="sxs-lookup"><span data-stu-id="65094-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="65094-107">Ezt a parancsot úgy kell kiállítani, hogy az előfizetésbe jelentkezzen be, ahol az az új kiszolgáló, amelyen az alias pont található.</span><span class="sxs-lookup"><span data-stu-id="65094-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="65094-108">Példák</span><span class="sxs-lookup"><span data-stu-id="65094-108">EXAMPLES</span></span>

### <span data-ttu-id="65094-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65094-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="65094-110">Ez a parancs olyan aliasokat frissít, amelyek korábban a oldServer mutattak, és a kiszolgáló newServer mutatnak</span><span class="sxs-lookup"><span data-stu-id="65094-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="65094-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65094-111">PARAMETERS</span></span>

### <span data-ttu-id="65094-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65094-112">-AsJob</span></span>
<span data-ttu-id="65094-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65094-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65094-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65094-114">-DefaultProfile</span></span>
<span data-ttu-id="65094-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65094-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65094-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65094-116">-Name</span></span>
<span data-ttu-id="65094-117">Az Azure SQL Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="65094-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65094-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65094-118">-ResourceGroupName</span></span>
<span data-ttu-id="65094-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="65094-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65094-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="65094-120">-SourceServerName</span></span>
<span data-ttu-id="65094-121">Annak az Azure SQL Server-kiszolgálónak a neve, amelyhez az alias jelenleg mutat.</span><span class="sxs-lookup"><span data-stu-id="65094-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65094-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65094-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="65094-123">A forráskiszolgáló erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="65094-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65094-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65094-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="65094-125">A forráskiszolgáló előfizetési azonosítója</span><span class="sxs-lookup"><span data-stu-id="65094-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65094-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="65094-126">-TargetServerName</span></span>
<span data-ttu-id="65094-127">Annak az Azure SQL Server-kiszolgálónak a neve, amelyhez az aliasnak mutatnia kell.</span><span class="sxs-lookup"><span data-stu-id="65094-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65094-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65094-128">-Confirm</span></span>
<span data-ttu-id="65094-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65094-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65094-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65094-130">-WhatIf</span></span>
<span data-ttu-id="65094-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65094-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65094-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65094-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65094-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65094-133">CommonParameters</span></span>
<span data-ttu-id="65094-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65094-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65094-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65094-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65094-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65094-136">INPUTS</span></span>

### <span data-ttu-id="65094-137">System. String</span><span class="sxs-lookup"><span data-stu-id="65094-137">System.String</span></span>

## <span data-ttu-id="65094-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65094-138">OUTPUTS</span></span>

### <span data-ttu-id="65094-139">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="65094-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="65094-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65094-140">NOTES</span></span>

## <span data-ttu-id="65094-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65094-141">RELATED LINKS</span></span>
