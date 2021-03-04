---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 46a3476d5ae4cead17eba0d03412ad2db57b01a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920218"
---
# <span data-ttu-id="0f3c6-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="0f3c6-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="0f3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3c6-103">Ez a parancs új Azure SQL Server DNS-aliast hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="0f3c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f3c6-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f3c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f3c6-105">DESCRIPTION</span></span>
<span data-ttu-id="0f3c6-106">Új Azure SQL Server DNS-aliast hoz létre, amely adott kiszolgálóra mutat.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="0f3c6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f3c6-107">EXAMPLES</span></span>

### <span data-ttu-id="0f3c6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0f3c6-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="0f3c6-109">Ez a parancs létrehozza az Azure SQL Server DNS-aliasát a serverName kiszolgálónévre mutató aliasnévvel</span><span class="sxs-lookup"><span data-stu-id="0f3c6-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="0f3c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f3c6-110">PARAMETERS</span></span>

### <span data-ttu-id="0f3c6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f3c6-111">-AsJob</span></span>
<span data-ttu-id="0f3c6-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f3c6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f3c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3c6-113">-DefaultProfile</span></span>
<span data-ttu-id="0f3c6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f3c6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0f3c6-115">-Name</span></span>
<span data-ttu-id="0f3c6-116">Az Azure Sql Server DNS-alias neve.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f3c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f3c6-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="0f3c6-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f3c6-119">-ServerName</span></span>
<span data-ttu-id="0f3c6-120">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0f3c6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f3c6-121">-Confirm</span></span>
<span data-ttu-id="0f3c6-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f3c6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f3c6-123">-WhatIf</span></span>
<span data-ttu-id="0f3c6-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f3c6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f3c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3c6-126">CommonParameters</span></span>
<span data-ttu-id="0f3c6-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3c6-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f3c6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3c6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f3c6-129">INPUTS</span></span>

### <span data-ttu-id="0f3c6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0f3c6-130">System.String</span></span>

## <span data-ttu-id="0f3c6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f3c6-131">OUTPUTS</span></span>

### <span data-ttu-id="0f3c6-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="0f3c6-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="0f3c6-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f3c6-133">NOTES</span></span>

## <span data-ttu-id="0f3c6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f3c6-134">RELATED LINKS</span></span>
