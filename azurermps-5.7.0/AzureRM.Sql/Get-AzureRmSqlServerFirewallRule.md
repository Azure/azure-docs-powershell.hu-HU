---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: eb514075bd366a0360f29c65455805be5f85569f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492140"
---
# <span data-ttu-id="fb010-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fb010-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="fb010-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb010-102">SYNOPSIS</span></span>
<span data-ttu-id="fb010-103">Tűzfal-szabályokat kap egy SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="fb010-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb010-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb010-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb010-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb010-105">DESCRIPTION</span></span>
<span data-ttu-id="fb010-106">A **Get-AzureRmSqlServerFirewallRule** parancsmag tűzfal-szabályokat kap az Azure SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="fb010-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="fb010-107">Ha megadhatja a tűzfalszabály nevét, ez a parancsmag információt kap az adott tűzfalszabály-szabályról.</span><span class="sxs-lookup"><span data-stu-id="fb010-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="fb010-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fb010-108">EXAMPLES</span></span>

### <span data-ttu-id="fb010-109">Példa 1: a kiszolgáló összes szabályának lekérése</span><span class="sxs-lookup"><span data-stu-id="fb010-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="fb010-110">Ez a parancs beolvassa a Server01 nevű kiszolgáló összes tűzfal-szabályát.</span><span class="sxs-lookup"><span data-stu-id="fb010-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="fb010-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb010-111">PARAMETERS</span></span>

### <span data-ttu-id="fb010-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb010-112">-DefaultProfile</span></span>
<span data-ttu-id="fb010-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb010-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb010-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="fb010-114">-FirewallRuleName</span></span>
<span data-ttu-id="fb010-115">A tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb010-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb010-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb010-116">-ResourceGroupName</span></span>
<span data-ttu-id="fb010-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="fb010-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb010-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fb010-118">-ServerName</span></span>
<span data-ttu-id="fb010-119">Az SQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb010-119">Specifies the name of the SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb010-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb010-120">-Confirm</span></span>
<span data-ttu-id="fb010-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb010-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb010-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb010-122">-WhatIf</span></span>
<span data-ttu-id="fb010-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb010-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb010-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb010-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb010-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb010-125">CommonParameters</span></span>
<span data-ttu-id="fb010-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb010-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb010-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb010-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb010-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb010-128">INPUTS</span></span>

### <span data-ttu-id="fb010-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb010-129">None</span></span>
<span data-ttu-id="fb010-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fb010-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb010-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb010-131">OUTPUTS</span></span>

### <span data-ttu-id="fb010-132">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="fb010-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="fb010-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb010-133">NOTES</span></span>

## <span data-ttu-id="fb010-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb010-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb010-135">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fb010-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="fb010-136">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fb010-136">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="fb010-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fb010-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="fb010-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fb010-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


