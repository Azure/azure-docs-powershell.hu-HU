---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 239e9325532b18140a36e4b8f9a8f291e508a91c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494070"
---
# <span data-ttu-id="36c16-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="36c16-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="36c16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36c16-102">SYNOPSIS</span></span>
<span data-ttu-id="36c16-103">Tűzfal szabályait eltávolítja egy adattó-fiókból.</span><span class="sxs-lookup"><span data-stu-id="36c16-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36c16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36c16-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36c16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36c16-105">DESCRIPTION</span></span>
<span data-ttu-id="36c16-106">A **Remove-AzureRmDataLakeAnalyticsFirewallRule** parancsmag az Azure Data-tó Analytics-fiókjából távolítja el a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="36c16-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="36c16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36c16-107">EXAMPLES</span></span>

### <span data-ttu-id="36c16-108">1. példa: tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36c16-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="36c16-109">Ez a parancs eltávolítja a "saját tűzfalszabályok" nevű tűzfal-szabályt a "ContosoAdlAcct" fiókból.</span><span class="sxs-lookup"><span data-stu-id="36c16-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="36c16-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36c16-110">PARAMETERS</span></span>

### <span data-ttu-id="36c16-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="36c16-111">-Account</span></span>
<span data-ttu-id="36c16-112">Az Data Lake Analytics-fiókja a tűzfalszabály eltávolításához</span><span class="sxs-lookup"><span data-stu-id="36c16-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c16-113">-DefaultProfile</span></span>
<span data-ttu-id="36c16-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36c16-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36c16-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36c16-115">-Name</span></span>
<span data-ttu-id="36c16-116">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="36c16-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c16-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36c16-117">-PassThru</span></span>
<span data-ttu-id="36c16-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="36c16-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c16-119">-ResourceGroupName</span></span>
<span data-ttu-id="36c16-120">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="36c16-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c16-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36c16-121">-Confirm</span></span>
<span data-ttu-id="36c16-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36c16-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36c16-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c16-123">-WhatIf</span></span>
<span data-ttu-id="36c16-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36c16-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36c16-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36c16-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36c16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c16-126">CommonParameters</span></span>
<span data-ttu-id="36c16-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36c16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c16-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c16-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c16-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36c16-129">INPUTS</span></span>

### <span data-ttu-id="36c16-130">System. String</span><span class="sxs-lookup"><span data-stu-id="36c16-130">System.String</span></span>

### <span data-ttu-id="36c16-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36c16-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36c16-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36c16-132">OUTPUTS</span></span>

### <span data-ttu-id="36c16-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36c16-133">System.Boolean</span></span>

## <span data-ttu-id="36c16-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36c16-134">NOTES</span></span>

## <span data-ttu-id="36c16-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36c16-135">RELATED LINKS</span></span>
