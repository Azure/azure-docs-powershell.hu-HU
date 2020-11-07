---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680738"
---
# <span data-ttu-id="35648-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="35648-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="35648-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35648-102">SYNOPSIS</span></span>
<span data-ttu-id="35648-103">Módosítja egy Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="35648-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35648-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35648-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35648-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="35648-105">DESCRIPTION</span></span>
<span data-ttu-id="35648-106">Ez a parancs módosítja egy Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="35648-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="35648-107">A kiszolgálón lévő virtuális hálózati szabályok beállításához használja inkább a "AzureRmSqlServerVirtualNetworkRule" és a "Remove-AzureRmSqlServerVirtualNetworkRule" parancsot.</span><span class="sxs-lookup"><span data-stu-id="35648-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="35648-108">Példák</span><span class="sxs-lookup"><span data-stu-id="35648-108">EXAMPLES</span></span>

### <span data-ttu-id="35648-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35648-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="35648-110">Módosítja egy meglévő virtuális hálózati szabályt az új virtuális hálózat alhálózati azonosítójával, amely az új virtuális hálózatról tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="35648-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="35648-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35648-111">PARAMETERS</span></span>

### <span data-ttu-id="35648-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35648-112">-ResourceGroupName</span></span>
<span data-ttu-id="35648-113">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35648-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="35648-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="35648-114">-ServerName</span></span>
<span data-ttu-id="35648-115">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="35648-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="35648-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="35648-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="35648-117">Az Azure SQL Server virtuális hálózati szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="35648-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="35648-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="35648-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="35648-119">A szabály virtuális hálózati alhálózati azonosítója.</span><span class="sxs-lookup"><span data-stu-id="35648-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="35648-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35648-120">-Confirm</span></span>
<span data-ttu-id="35648-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35648-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35648-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35648-122">-WhatIf</span></span>
<span data-ttu-id="35648-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35648-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35648-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35648-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35648-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35648-125">-DefaultProfile</span></span>
<span data-ttu-id="35648-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35648-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35648-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35648-127">CommonParameters</span></span>
<span data-ttu-id="35648-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35648-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35648-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35648-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35648-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35648-130">INPUTS</span></span>

### <span data-ttu-id="35648-131">System. String</span><span class="sxs-lookup"><span data-stu-id="35648-131">System.String</span></span>

## <span data-ttu-id="35648-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35648-132">OUTPUTS</span></span>

### <span data-ttu-id="35648-133">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="35648-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="35648-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35648-134">NOTES</span></span>

## <span data-ttu-id="35648-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35648-135">RELATED LINKS</span></span>

