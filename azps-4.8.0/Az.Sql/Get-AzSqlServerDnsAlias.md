---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180823"
---
# <span data-ttu-id="540a9-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="540a9-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="540a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="540a9-102">SYNOPSIS</span></span>
<span data-ttu-id="540a9-103">Azure SQL Server DNS-aliast kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="540a9-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="540a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="540a9-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="540a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="540a9-105">DESCRIPTION</span></span>
<span data-ttu-id="540a9-106">A megadott Azure SQL Server DNS-alias beszerzése vagy a kiszolgáló összes DNS-aliasának listázása</span><span class="sxs-lookup"><span data-stu-id="540a9-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="540a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="540a9-107">EXAMPLES</span></span>

### <span data-ttu-id="540a9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="540a9-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="540a9-109">A kiszolgáló összes DNS-aliasának listázása az adott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="540a9-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="540a9-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="540a9-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="540a9-111">A kiszolgáló és az alias neve által megadott DNS-alias beolvasása</span><span class="sxs-lookup"><span data-stu-id="540a9-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="540a9-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="540a9-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="540a9-113">A "dnsaliasname" kezdetű kiszolgáló DNS-aliasait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="540a9-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="540a9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="540a9-114">PARAMETERS</span></span>

### <span data-ttu-id="540a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540a9-115">-DefaultProfile</span></span>
<span data-ttu-id="540a9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="540a9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="540a9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="540a9-117">-Name</span></span>
<span data-ttu-id="540a9-118">Az Azure SQL Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="540a9-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="540a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="540a9-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="540a9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="540a9-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="540a9-121">-ServerName</span></span>
<span data-ttu-id="540a9-122">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="540a9-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="540a9-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="540a9-123">-Confirm</span></span>
<span data-ttu-id="540a9-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="540a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540a9-125">-WhatIf</span></span>
<span data-ttu-id="540a9-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="540a9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540a9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="540a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540a9-128">CommonParameters</span></span>
<span data-ttu-id="540a9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="540a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540a9-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="540a9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540a9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="540a9-131">INPUTS</span></span>

### <span data-ttu-id="540a9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="540a9-132">System.String</span></span>

## <span data-ttu-id="540a9-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="540a9-133">OUTPUTS</span></span>

### <span data-ttu-id="540a9-134">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="540a9-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="540a9-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="540a9-135">NOTES</span></span>

## <span data-ttu-id="540a9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="540a9-136">RELATED LINKS</span></span>
