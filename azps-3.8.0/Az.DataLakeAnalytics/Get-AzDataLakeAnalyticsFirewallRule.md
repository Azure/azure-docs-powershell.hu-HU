---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010845"
---
# <span data-ttu-id="20ece-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20ece-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="20ece-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20ece-102">SYNOPSIS</span></span>
<span data-ttu-id="20ece-103">Tűzfal-szabály vagy tűzfalszabályok listájának beolvasása egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="20ece-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="20ece-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20ece-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20ece-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20ece-105">DESCRIPTION</span></span>
<span data-ttu-id="20ece-106">A **Get-AzDataLakeAnalyticsFirewallRule** parancsmag az Azure Data Lake Analytics-fiókból letölti a tűzfalszabályok vagy a tűzfalszabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="20ece-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="20ece-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20ece-107">EXAMPLES</span></span>

### <span data-ttu-id="20ece-108">Példa 1: tűzfalszabály beszerzése</span><span class="sxs-lookup"><span data-stu-id="20ece-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="20ece-109">Ez a parancs a "My Firewall Rule" nevű tűzfal-szabályt kapja meg a "ContosoAdlAcct" fiókból.</span><span class="sxs-lookup"><span data-stu-id="20ece-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="20ece-110">2. példa: az összes tűzfal-szabály listázása</span><span class="sxs-lookup"><span data-stu-id="20ece-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="20ece-111">Ez a parancs a "ContosoAdlAcct" fiókból kapja meg az összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="20ece-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="20ece-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20ece-112">PARAMETERS</span></span>

### <span data-ttu-id="20ece-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="20ece-113">-Account</span></span>
<span data-ttu-id="20ece-114">Az Data Lake Analytics-fiókja a tűzfalszabály beszerzéséhez</span><span class="sxs-lookup"><span data-stu-id="20ece-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="20ece-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ece-115">-DefaultProfile</span></span>
<span data-ttu-id="20ece-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="20ece-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20ece-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20ece-117">-Name</span></span>
<span data-ttu-id="20ece-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="20ece-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="20ece-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ece-119">-ResourceGroupName</span></span>
<span data-ttu-id="20ece-120">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="20ece-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="20ece-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ece-121">CommonParameters</span></span>
<span data-ttu-id="20ece-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20ece-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ece-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ece-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ece-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20ece-124">INPUTS</span></span>

### <span data-ttu-id="20ece-125">System. String</span><span class="sxs-lookup"><span data-stu-id="20ece-125">System.String</span></span>

## <span data-ttu-id="20ece-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20ece-126">OUTPUTS</span></span>

### <span data-ttu-id="20ece-127">Microsoft. Azure. Command. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20ece-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="20ece-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20ece-128">NOTES</span></span>

## <span data-ttu-id="20ece-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20ece-129">RELATED LINKS</span></span>
