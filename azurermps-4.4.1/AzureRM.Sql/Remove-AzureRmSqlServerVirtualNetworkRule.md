---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680752"
---
# <span data-ttu-id="ca3bb-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ca3bb-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="ca3bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3bb-103">Azure SQL Server virtuális hálózati szabály törlése</span><span class="sxs-lookup"><span data-stu-id="ca3bb-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca3bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca3bb-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca3bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca3bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ca3bb-106">Ez a parancs törli az Azure SQL Server virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="ca3bb-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="ca3bb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca3bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ca3bb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca3bb-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="ca3bb-109">Meglévő Azure SQL Server-alapú virtuális hálózati szabály törlése</span><span class="sxs-lookup"><span data-stu-id="ca3bb-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="ca3bb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca3bb-110">PARAMETERS</span></span>

### <span data-ttu-id="ca3bb-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca3bb-111">-ResourceGroupName</span></span>
<span data-ttu-id="ca3bb-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ca3bb-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca3bb-113">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ca3bb-113">-ServerName</span></span>
<span data-ttu-id="ca3bb-114">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ca3bb-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ca3bb-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="ca3bb-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="ca3bb-116">Azure SQL Server virtuális hálózati szabály neve</span><span class="sxs-lookup"><span data-stu-id="ca3bb-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="ca3bb-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca3bb-117">-Confirm</span></span>
<span data-ttu-id="ca3bb-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca3bb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3bb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3bb-119">-WhatIf</span></span>
<span data-ttu-id="ca3bb-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca3bb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca3bb-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca3bb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3bb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3bb-122">-DefaultProfile</span></span>
<span data-ttu-id="ca3bb-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca3bb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca3bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3bb-124">CommonParameters</span></span>
<span data-ttu-id="ca3bb-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca3bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3bb-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca3bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3bb-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca3bb-127">INPUTS</span></span>

### <span data-ttu-id="ca3bb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ca3bb-128">System.String</span></span>

## <span data-ttu-id="ca3bb-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca3bb-129">OUTPUTS</span></span>

### <span data-ttu-id="ca3bb-130">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="ca3bb-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="ca3bb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca3bb-131">NOTES</span></span>

## <span data-ttu-id="ca3bb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca3bb-132">RELATED LINKS</span></span>

