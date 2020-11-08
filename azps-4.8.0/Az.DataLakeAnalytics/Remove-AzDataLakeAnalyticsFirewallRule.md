---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025406"
---
# <span data-ttu-id="0612d-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0612d-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0612d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0612d-102">SYNOPSIS</span></span>
<span data-ttu-id="0612d-103">Tűzfal szabályait eltávolítja egy adattó-fiókból.</span><span class="sxs-lookup"><span data-stu-id="0612d-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0612d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0612d-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0612d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0612d-105">DESCRIPTION</span></span>
<span data-ttu-id="0612d-106">A **Remove-AzDataLakeAnalyticsFirewallRule** parancsmag az Azure Data-tó Analytics-fiókjából távolítja el a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="0612d-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0612d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0612d-107">EXAMPLES</span></span>

### <span data-ttu-id="0612d-108">1. példa: tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0612d-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="0612d-109">Ez a parancs eltávolítja a "saját tűzfalszabályok" nevű tűzfal-szabályt a "ContosoAdlAcct" fiókból.</span><span class="sxs-lookup"><span data-stu-id="0612d-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="0612d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0612d-110">PARAMETERS</span></span>

### <span data-ttu-id="0612d-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="0612d-111">-Account</span></span>
<span data-ttu-id="0612d-112">Az Data Lake Analytics-fiókja a tűzfalszabály eltávolításához</span><span class="sxs-lookup"><span data-stu-id="0612d-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="0612d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0612d-113">-DefaultProfile</span></span>
<span data-ttu-id="0612d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0612d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0612d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0612d-115">-Name</span></span>
<span data-ttu-id="0612d-116">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="0612d-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="0612d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0612d-117">-PassThru</span></span>
<span data-ttu-id="0612d-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0612d-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0612d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0612d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0612d-120">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="0612d-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="0612d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0612d-121">-Confirm</span></span>
<span data-ttu-id="0612d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0612d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0612d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0612d-123">-WhatIf</span></span>
<span data-ttu-id="0612d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0612d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0612d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0612d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0612d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0612d-126">CommonParameters</span></span>
<span data-ttu-id="0612d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0612d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0612d-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0612d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0612d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0612d-129">INPUTS</span></span>

### <span data-ttu-id="0612d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0612d-130">System.String</span></span>

### <span data-ttu-id="0612d-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0612d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0612d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0612d-132">OUTPUTS</span></span>

### <span data-ttu-id="0612d-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0612d-133">System.Boolean</span></span>

## <span data-ttu-id="0612d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0612d-134">NOTES</span></span>

## <span data-ttu-id="0612d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0612d-135">RELATED LINKS</span></span>
