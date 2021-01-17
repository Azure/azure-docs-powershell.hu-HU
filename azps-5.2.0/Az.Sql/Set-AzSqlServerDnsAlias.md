---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343962"
---
# <span data-ttu-id="000c0-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="000c0-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="000c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="000c0-102">SYNOPSIS</span></span>
<span data-ttu-id="000c0-103">Módosítja azt a kiszolgálót, amelyre az Azure SQL Server DNS-aliasa mutat</span><span class="sxs-lookup"><span data-stu-id="000c0-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="000c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="000c0-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="000c0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="000c0-105">DESCRIPTION</span></span>
<span data-ttu-id="000c0-106">Ez a parancs frissíti azt a kiszolgálót, amelyre az alias mutat.</span><span class="sxs-lookup"><span data-stu-id="000c0-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="000c0-107">Ezt a parancsot akkor kell kiadni, amikor bejelentkezik az előfizetésbe, ahol az új kiszolgáló, amelyre az alias fog mutasson, megtalálható.</span><span class="sxs-lookup"><span data-stu-id="000c0-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="000c0-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="000c0-108">EXAMPLES</span></span>

### <span data-ttu-id="000c0-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="000c0-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="000c0-110">Ez a parancs frissíti az aliast, amely korábban a régiServerre mutatott, hogy az új kiszolgálóra mutasson</span><span class="sxs-lookup"><span data-stu-id="000c0-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="000c0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="000c0-111">PARAMETERS</span></span>

### <span data-ttu-id="000c0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="000c0-112">-AsJob</span></span>
<span data-ttu-id="000c0-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="000c0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="000c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000c0-114">-DefaultProfile</span></span>
<span data-ttu-id="000c0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="000c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="000c0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="000c0-116">-Name</span></span>
<span data-ttu-id="000c0-117">Az Azure Sql Server DNS-alias neve.</span><span class="sxs-lookup"><span data-stu-id="000c0-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="000c0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="000c0-118">-ResourceGroupName</span></span>
<span data-ttu-id="000c0-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="000c0-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="000c0-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="000c0-120">-SourceServerName</span></span>
<span data-ttu-id="000c0-121">Annak az Azure Sql Servernek a neve, amelyre az alias jelenleg mutat.</span><span class="sxs-lookup"><span data-stu-id="000c0-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="000c0-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="000c0-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="000c0-123">A forráskiszolgáló erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="000c0-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="000c0-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="000c0-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="000c0-125">A forráskiszolgáló előfizetésazonosítója</span><span class="sxs-lookup"><span data-stu-id="000c0-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="000c0-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="000c0-126">-TargetServerName</span></span>
<span data-ttu-id="000c0-127">Az Azure Sql Server neve, amelyre az aliasnak kell mutasson.</span><span class="sxs-lookup"><span data-stu-id="000c0-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="000c0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="000c0-128">-Confirm</span></span>
<span data-ttu-id="000c0-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="000c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="000c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="000c0-130">-WhatIf</span></span>
<span data-ttu-id="000c0-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="000c0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="000c0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="000c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="000c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000c0-133">CommonParameters</span></span>
<span data-ttu-id="000c0-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="000c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000c0-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="000c0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000c0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="000c0-136">INPUTS</span></span>

### <span data-ttu-id="000c0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="000c0-137">System.String</span></span>

## <span data-ttu-id="000c0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="000c0-138">OUTPUTS</span></span>

### <span data-ttu-id="000c0-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="000c0-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="000c0-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="000c0-140">NOTES</span></span>

## <span data-ttu-id="000c0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="000c0-141">RELATED LINKS</span></span>
