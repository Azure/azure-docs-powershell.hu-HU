---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480365"
---
# <span data-ttu-id="6e71d-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e71d-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6e71d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e71d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e71d-103">Tűzfalszabályt vagy tűzfalszabályok listáját olvassa be egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="6e71d-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6e71d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e71d-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e71d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e71d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e71d-106">A **Get-AzDataLakeAnalyticsFirewallRule parancsmag** egy tűzfalszabályt vagy tűzfalszabályok listáját olvassa be egy Azure Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="6e71d-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6e71d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e71d-107">EXAMPLES</span></span>

### <span data-ttu-id="6e71d-108">1. példa: Tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="6e71d-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="6e71d-109">Ez a parancs a "Saját tűzfalszabály" nevű tűzfalszabályt a "ContosoAdlAcct" fiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6e71d-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="6e71d-110">2. példa: Az összes tűzfalszabály felsorolása</span><span class="sxs-lookup"><span data-stu-id="6e71d-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="6e71d-111">Ez a parancs az összes tűzfalszabályt a "ContosoAdlAcct" fiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6e71d-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="6e71d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e71d-112">PARAMETERS</span></span>

### <span data-ttu-id="6e71d-113">-Account</span><span class="sxs-lookup"><span data-stu-id="6e71d-113">-Account</span></span>
<span data-ttu-id="6e71d-114">The Data Lake Analytics account to get the firewall rule from</span><span class="sxs-lookup"><span data-stu-id="6e71d-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="6e71d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e71d-115">-DefaultProfile</span></span>
<span data-ttu-id="6e71d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e71d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e71d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6e71d-117">-Name</span></span>
<span data-ttu-id="6e71d-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="6e71d-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="6e71d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e71d-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e71d-120">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="6e71d-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e71d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e71d-121">CommonParameters</span></span>
<span data-ttu-id="6e71d-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e71d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e71d-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e71d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e71d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e71d-124">INPUTS</span></span>

### <span data-ttu-id="6e71d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6e71d-125">System.String</span></span>

## <span data-ttu-id="6e71d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e71d-126">OUTPUTS</span></span>

### <span data-ttu-id="6e71d-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e71d-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6e71d-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e71d-128">NOTES</span></span>

## <span data-ttu-id="6e71d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e71d-129">RELATED LINKS</span></span>
