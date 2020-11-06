---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: cc85bea2739c379e960ffee29250bdc172e36765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495608"
---
# <span data-ttu-id="ee204-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="ee204-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="ee204-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee204-102">SYNOPSIS</span></span>
<span data-ttu-id="ee204-103">Azure SQL Server DNS-aliast kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="ee204-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee204-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee204-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee204-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee204-105">DESCRIPTION</span></span>
<span data-ttu-id="ee204-106">A megadott Azure SQL Server DNS-alias beszerzése vagy a kiszolgáló összes DNS-aliasának listázása</span><span class="sxs-lookup"><span data-stu-id="ee204-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="ee204-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee204-107">EXAMPLES</span></span>

### <span data-ttu-id="ee204-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ee204-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="ee204-109">A kiszolgáló összes DNS-aliasának listázása az adott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="ee204-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="ee204-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="ee204-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="ee204-111">A kiszolgáló és az alias neve által megadott DNS-alias beolvasása</span><span class="sxs-lookup"><span data-stu-id="ee204-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="ee204-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee204-112">PARAMETERS</span></span>

### <span data-ttu-id="ee204-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee204-113">-DefaultProfile</span></span>
<span data-ttu-id="ee204-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee204-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee204-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee204-115">-Name</span></span>
<span data-ttu-id="ee204-116">Az Azure SQL Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="ee204-116">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="ee204-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee204-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee204-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee204-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee204-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ee204-119">-ServerName</span></span>
<span data-ttu-id="ee204-120">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ee204-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ee204-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee204-121">-Confirm</span></span>
<span data-ttu-id="ee204-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee204-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee204-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee204-123">-WhatIf</span></span>
<span data-ttu-id="ee204-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee204-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee204-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee204-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee204-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee204-126">CommonParameters</span></span>
<span data-ttu-id="ee204-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee204-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee204-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee204-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee204-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee204-129">INPUTS</span></span>

### <span data-ttu-id="ee204-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ee204-130">System.String</span></span>

## <span data-ttu-id="ee204-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee204-131">OUTPUTS</span></span>

### <span data-ttu-id="ee204-132">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="ee204-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="ee204-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee204-133">NOTES</span></span>

## <span data-ttu-id="ee204-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee204-134">RELATED LINKS</span></span>
