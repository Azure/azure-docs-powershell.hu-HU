---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 68fb8bac3a492bec915af6aea7df5d67fc3668dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492718"
---
# <span data-ttu-id="821e3-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="821e3-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="821e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="821e3-102">SYNOPSIS</span></span>
<span data-ttu-id="821e3-103">Azure SQL Server virtuális hálózati szabály beolvasása vagy listázása.</span><span class="sxs-lookup"><span data-stu-id="821e3-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="821e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="821e3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="821e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="821e3-105">DESCRIPTION</span></span>
<span data-ttu-id="821e3-106">Ez a parancs egy bizonyos Azure SQL Server virtuális hálózati szabályt vagy az Azure SQL Server virtuális hálózati szabályait tartalmazó listát kap a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="821e3-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="821e3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="821e3-107">EXAMPLES</span></span>

### <span data-ttu-id="821e3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="821e3-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="821e3-109">Egyetlen Azure SQL Server-alapú virtuális hálózati szabály kap</span><span class="sxs-lookup"><span data-stu-id="821e3-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="821e3-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="821e3-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="821e3-111">Az Azure SQL Server virtuális hálózati szabályainak listája a megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="821e3-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="821e3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="821e3-112">PARAMETERS</span></span>

### <span data-ttu-id="821e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821e3-113">-DefaultProfile</span></span>
<span data-ttu-id="821e3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="821e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="821e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="821e3-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="821e3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="821e3-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="821e3-117">-ServerName</span></span>
<span data-ttu-id="821e3-118">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="821e3-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="821e3-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="821e3-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="821e3-120">Az Azure SQL Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="821e3-120">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821e3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821e3-121">CommonParameters</span></span>
<span data-ttu-id="821e3-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="821e3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821e3-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="821e3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821e3-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="821e3-124">INPUTS</span></span>

### <span data-ttu-id="821e3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="821e3-125">System.String</span></span>

## <span data-ttu-id="821e3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="821e3-126">OUTPUTS</span></span>

### <span data-ttu-id="821e3-127">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="821e3-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="821e3-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="821e3-128">NOTES</span></span>

## <span data-ttu-id="821e3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="821e3-129">RELATED LINKS</span></span>
