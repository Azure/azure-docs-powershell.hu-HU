---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 3e0f7e021f6ddf2f9b18873dda4f9d482a4db1da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680302"
---
# <span data-ttu-id="a06a9-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a06a9-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="a06a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a06a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a06a9-103">Tűzfal-szabály törlése SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="a06a9-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a06a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a06a9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a06a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a06a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a06a9-106">A **Remove-AzureRmSqlServerFirewallRule** parancsmag a megadott Azure SQL adatbázis-kiszolgálóról törli a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="a06a9-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="a06a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a06a9-107">EXAMPLES</span></span>

### <span data-ttu-id="a06a9-108">Példa 1: szabály törlése</span><span class="sxs-lookup"><span data-stu-id="a06a9-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a06a9-109">Ez a parancs törli a Rule01 nevű tűzfal-szabályt a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="a06a9-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="a06a9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a06a9-110">PARAMETERS</span></span>

### <span data-ttu-id="a06a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06a9-111">-DefaultProfile</span></span>
<span data-ttu-id="a06a9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a06a9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a06a9-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a06a9-113">-FirewallRuleName</span></span>
<span data-ttu-id="a06a9-114">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="a06a9-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06a9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a06a9-115">-Force</span></span>
<span data-ttu-id="a06a9-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a06a9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a06a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a06a9-118">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="a06a9-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a06a9-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a06a9-119">-ServerName</span></span>
<span data-ttu-id="a06a9-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a06a9-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a06a9-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a06a9-121">-Confirm</span></span>
<span data-ttu-id="a06a9-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a06a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a06a9-123">-WhatIf</span></span>
<span data-ttu-id="a06a9-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a06a9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a06a9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a06a9-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06a9-126">CommonParameters</span></span>
<span data-ttu-id="a06a9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a06a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06a9-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06a9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a06a9-129">INPUTS</span></span>

### <span data-ttu-id="a06a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a06a9-130">System.String</span></span>

## <span data-ttu-id="a06a9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a06a9-131">OUTPUTS</span></span>

### <span data-ttu-id="a06a9-132">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="a06a9-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a06a9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a06a9-133">NOTES</span></span>

## <span data-ttu-id="a06a9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a06a9-134">RELATED LINKS</span></span>

[<span data-ttu-id="a06a9-135">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a06a9-135">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a06a9-136">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a06a9-136">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a06a9-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a06a9-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a06a9-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a06a9-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


