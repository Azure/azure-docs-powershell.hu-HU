---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: e95d29b5a91f8df257649693bdd9d4029ca3d166
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942802"
---
# <span data-ttu-id="0314c-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0314c-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0314c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0314c-102">SYNOPSIS</span></span>
<span data-ttu-id="0314c-103">Tűzfalszabályt vagy tűzfalszabályok listáját olvassa be egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="0314c-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0314c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0314c-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0314c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0314c-105">DESCRIPTION</span></span>
<span data-ttu-id="0314c-106">A **Get-AzDataLakeAnalyticsFirewallRule parancsmag** egy tűzfalszabályt vagy tűzfalszabályok listáját olvassa be egy Azure Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="0314c-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0314c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0314c-107">EXAMPLES</span></span>

### <span data-ttu-id="0314c-108">1. példa: Tűzfalszabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="0314c-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="0314c-109">Ez a parancs a "Saját tűzfalszabály" nevű tűzfalszabályt a "ContosoAdlAcct" fiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0314c-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="0314c-110">2. példa: Az összes tűzfalszabály felsorolása</span><span class="sxs-lookup"><span data-stu-id="0314c-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="0314c-111">Ez a parancs az összes tűzfalszabályt a "ContosoAdlAcct" fiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0314c-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="0314c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0314c-112">PARAMETERS</span></span>

### <span data-ttu-id="0314c-113">-Account</span><span class="sxs-lookup"><span data-stu-id="0314c-113">-Account</span></span>
<span data-ttu-id="0314c-114">The Data Lake Analytics account to get the firewall rule from</span><span class="sxs-lookup"><span data-stu-id="0314c-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="0314c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0314c-115">-DefaultProfile</span></span>
<span data-ttu-id="0314c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0314c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0314c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0314c-117">-Name</span></span>
<span data-ttu-id="0314c-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="0314c-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="0314c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0314c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0314c-120">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="0314c-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="0314c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0314c-121">CommonParameters</span></span>
<span data-ttu-id="0314c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0314c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0314c-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0314c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0314c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0314c-124">INPUTS</span></span>

### <span data-ttu-id="0314c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0314c-125">System.String</span></span>

## <span data-ttu-id="0314c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0314c-126">OUTPUTS</span></span>

### <span data-ttu-id="0314c-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0314c-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0314c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0314c-128">NOTES</span></span>

## <span data-ttu-id="0314c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0314c-129">RELATED LINKS</span></span>
