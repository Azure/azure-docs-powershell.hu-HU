---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343902"
---
# <span data-ttu-id="10bdc-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10bdc-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="10bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="10bdc-103">Eltávolít egy tűzfalszabályt egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="10bdc-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="10bdc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10bdc-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10bdc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="10bdc-106">A **Remove-AzDataLakeAnalyticsFirewallRule** parancsmag eltávolít egy tűzfalszabályt egy Azure Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="10bdc-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="10bdc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10bdc-107">EXAMPLES</span></span>

### <span data-ttu-id="10bdc-108">1. példa: Tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="10bdc-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="10bdc-109">Ez a parancs eltávolítja a "saját tűzfalszabály" nevű tűzfalszabályt a "ContosoAdlAcct" fiókból.</span><span class="sxs-lookup"><span data-stu-id="10bdc-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="10bdc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10bdc-110">PARAMETERS</span></span>

### <span data-ttu-id="10bdc-111">-Account</span><span class="sxs-lookup"><span data-stu-id="10bdc-111">-Account</span></span>
<span data-ttu-id="10bdc-112">The Data Lake Analytics account to remove the firewall rule from</span><span class="sxs-lookup"><span data-stu-id="10bdc-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="10bdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bdc-113">-DefaultProfile</span></span>
<span data-ttu-id="10bdc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="10bdc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10bdc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="10bdc-115">-Name</span></span>
<span data-ttu-id="10bdc-116">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="10bdc-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="10bdc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10bdc-117">-PassThru</span></span>
<span data-ttu-id="10bdc-118">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="10bdc-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="10bdc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bdc-119">-ResourceGroupName</span></span>
<span data-ttu-id="10bdc-120">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="10bdc-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="10bdc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10bdc-121">-Confirm</span></span>
<span data-ttu-id="10bdc-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="10bdc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10bdc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10bdc-123">-WhatIf</span></span>
<span data-ttu-id="10bdc-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="10bdc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10bdc-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10bdc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10bdc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bdc-126">CommonParameters</span></span>
<span data-ttu-id="10bdc-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10bdc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bdc-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10bdc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bdc-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10bdc-129">INPUTS</span></span>

### <span data-ttu-id="10bdc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="10bdc-130">System.String</span></span>

### <span data-ttu-id="10bdc-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10bdc-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10bdc-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10bdc-132">OUTPUTS</span></span>

### <span data-ttu-id="10bdc-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10bdc-133">System.Boolean</span></span>

## <span data-ttu-id="10bdc-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10bdc-134">NOTES</span></span>

## <span data-ttu-id="10bdc-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10bdc-135">RELATED LINKS</span></span>
