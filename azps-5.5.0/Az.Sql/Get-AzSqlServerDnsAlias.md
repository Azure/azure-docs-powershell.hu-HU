---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155315"
---
# <span data-ttu-id="c9b7b-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="c9b7b-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="c9b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b7b-103">Lekérte vagy felsorolja az Azure SQL Server DNS-aliasát.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="c9b7b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9b7b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b7b-106">Szerezze be az adott Azure SQL Server DNS-aliast, vagy sorolja fel a kiszolgáló összes kiszolgálói DNS-aliasát</span><span class="sxs-lookup"><span data-stu-id="c9b7b-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="c9b7b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b7b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c9b7b-109">Az adott kiszolgáló összes dns-aliasának listája</span><span class="sxs-lookup"><span data-stu-id="c9b7b-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="c9b7b-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="c9b7b-111">Kiszolgáló és aliasnév szerint megadott kiszolgáló DNS-aliast kap</span><span class="sxs-lookup"><span data-stu-id="c9b7b-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="c9b7b-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c9b7b-113">Az adott kiszolgáló "dnsaliasname" kezdetű kiszolgálói DNS-aliasai.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="c9b7b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-114">PARAMETERS</span></span>

### <span data-ttu-id="c9b7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b7b-115">-DefaultProfile</span></span>
<span data-ttu-id="c9b7b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9b7b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c9b7b-117">-Name</span></span>
<span data-ttu-id="c9b7b-118">Az Azure Sql Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b7b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9b7b-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9b7b-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9b7b-121">-ServerName</span></span>
<span data-ttu-id="c9b7b-122">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c9b7b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9b7b-123">-Confirm</span></span>
<span data-ttu-id="c9b7b-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b7b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b7b-125">-WhatIf</span></span>
<span data-ttu-id="c9b7b-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b7b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b7b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b7b-128">CommonParameters</span></span>
<span data-ttu-id="c9b7b-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b7b-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9b7b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b7b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-131">INPUTS</span></span>

### <span data-ttu-id="c9b7b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c9b7b-132">System.String</span></span>

## <span data-ttu-id="c9b7b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-133">OUTPUTS</span></span>

### <span data-ttu-id="c9b7b-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="c9b7b-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="c9b7b-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-135">NOTES</span></span>

## <span data-ttu-id="c9b7b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-136">RELATED LINKS</span></span>
