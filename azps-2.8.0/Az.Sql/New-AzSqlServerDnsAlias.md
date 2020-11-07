---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 60790af3396177e2885b4a83fda4d24db8c4e4d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839409"
---
# <span data-ttu-id="3f0ad-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="3f0ad-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="3f0ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0ad-103">A parancs létrehoz egy új Azure SQL Server DNS-aliast.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="3f0ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f0ad-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f0ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f0ad-105">DESCRIPTION</span></span>
<span data-ttu-id="3f0ad-106">Új Azure SQL Server DNS-Alias létrehozása, amely a megadott kiszolgálón van mutatva.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="3f0ad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f0ad-107">EXAMPLES</span></span>

### <span data-ttu-id="3f0ad-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3f0ad-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="3f0ad-109">Ez a parancs Azure SQL Server DNS-aliast hoz létre a kiszolgáló kiszolgálónév nevű aliasName.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="3f0ad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f0ad-110">PARAMETERS</span></span>

### <span data-ttu-id="3f0ad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f0ad-111">-AsJob</span></span>
<span data-ttu-id="3f0ad-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f0ad-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f0ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0ad-113">-DefaultProfile</span></span>
<span data-ttu-id="3f0ad-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f0ad-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f0ad-115">-Name</span></span>
<span data-ttu-id="3f0ad-116">Az Azure SQL Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="3f0ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f0ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f0ad-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f0ad-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3f0ad-119">-ServerName</span></span>
<span data-ttu-id="3f0ad-120">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3f0ad-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f0ad-121">-Confirm</span></span>
<span data-ttu-id="3f0ad-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f0ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f0ad-123">-WhatIf</span></span>
<span data-ttu-id="3f0ad-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f0ad-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f0ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0ad-126">CommonParameters</span></span>
<span data-ttu-id="3f0ad-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f0ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0ad-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f0ad-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0ad-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f0ad-129">INPUTS</span></span>

### <span data-ttu-id="3f0ad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3f0ad-130">System.String</span></span>

## <span data-ttu-id="3f0ad-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f0ad-131">OUTPUTS</span></span>

### <span data-ttu-id="3f0ad-132">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="3f0ad-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="3f0ad-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f0ad-133">NOTES</span></span>

## <span data-ttu-id="3f0ad-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f0ad-134">RELATED LINKS</span></span>
