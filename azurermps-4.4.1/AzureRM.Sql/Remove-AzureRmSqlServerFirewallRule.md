---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 1f7f039bb0bba1338fdcc4d5ceb3a403822fba71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493317"
---
# <span data-ttu-id="c9a9f-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9a9f-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="c9a9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a9f-103">Tűzfal-szabály törlése SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9a9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9a9f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9a9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9a9f-105">DESCRIPTION</span></span>
<span data-ttu-id="c9a9f-106">A **Remove-AzureRmSqlServerFirewallRule** parancsmag a megadott Azure SQL adatbázis-kiszolgálóról törli a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="c9a9f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9a9f-107">EXAMPLES</span></span>

### <span data-ttu-id="c9a9f-108">Példa 1: szabály törlése</span><span class="sxs-lookup"><span data-stu-id="c9a9f-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c9a9f-109">Ez a parancs törli a Rule01 nevű tűzfal-szabályt a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="c9a9f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9a9f-110">PARAMETERS</span></span>

### <span data-ttu-id="c9a9f-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="c9a9f-111">-FirewallRuleName</span></span>
<span data-ttu-id="c9a9f-112">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-112">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c9a9f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c9a9f-113">-Force</span></span>
<span data-ttu-id="c9a9f-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9a9f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a9f-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9a9f-116">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-116">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c9a9f-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c9a9f-117">-ServerName</span></span>
<span data-ttu-id="c9a9f-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c9a9f-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9a9f-119">-Confirm</span></span>
<span data-ttu-id="c9a9f-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a9f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a9f-121">-WhatIf</span></span>
<span data-ttu-id="c9a9f-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9a9f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a9f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a9f-124">-DefaultProfile</span></span>
<span data-ttu-id="c9a9f-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9a9f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9a9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a9f-126">CommonParameters</span></span>
<span data-ttu-id="c9a9f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9a9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a9f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9a9f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a9f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9a9f-129">INPUTS</span></span>

### <span data-ttu-id="c9a9f-130">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="c9a9f-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="c9a9f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9a9f-131">OUTPUTS</span></span>

## <span data-ttu-id="c9a9f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9a9f-132">NOTES</span></span>

## <span data-ttu-id="c9a9f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9a9f-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9a9f-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9a9f-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c9a9f-135">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9a9f-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c9a9f-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9a9f-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c9a9f-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c9a9f-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


