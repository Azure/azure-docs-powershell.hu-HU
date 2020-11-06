---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 99acce24389a02c8fb50f5b313841319f813feaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505079"
---
# <span data-ttu-id="c2060-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c2060-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="c2060-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2060-102">SYNOPSIS</span></span>
<span data-ttu-id="c2060-103">Tűzfal-szabály vagy tűzfalszabályok listájának beolvasása egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="c2060-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2060-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2060-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2060-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2060-105">DESCRIPTION</span></span>
<span data-ttu-id="c2060-106">A **Get-AzureRmDataLakeAnalyticsFirewallRule** parancsmag az Azure Data Lake Analytics-fiókból letölti a tűzfalszabályok vagy a tűzfalszabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="c2060-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c2060-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c2060-107">EXAMPLES</span></span>

### <span data-ttu-id="c2060-108">Példa 1: tűzfalszabály beszerzése</span><span class="sxs-lookup"><span data-stu-id="c2060-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="c2060-109">Ez a parancs a "My Firewall Rule" nevű tűzfal-szabályt kapja meg a "ContosoAdlAcct" fiókból.</span><span class="sxs-lookup"><span data-stu-id="c2060-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="c2060-110">2. példa: az összes tűzfal-szabály listázása</span><span class="sxs-lookup"><span data-stu-id="c2060-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="c2060-111">Ez a parancs a "ContosoAdlAcct" fiókból kapja meg az összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="c2060-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="c2060-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2060-112">PARAMETERS</span></span>

### <span data-ttu-id="c2060-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c2060-113">-Account</span></span>
<span data-ttu-id="c2060-114">Az Data Lake Analytics-fiókja a tűzfalszabály beszerzéséhez</span><span class="sxs-lookup"><span data-stu-id="c2060-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="c2060-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2060-115">-Name</span></span>
<span data-ttu-id="c2060-116">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="c2060-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="c2060-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2060-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2060-118">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="c2060-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="c2060-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2060-119">-DefaultProfile</span></span>
<span data-ttu-id="c2060-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2060-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2060-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2060-121">CommonParameters</span></span>
<span data-ttu-id="c2060-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2060-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2060-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2060-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2060-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2060-124">INPUTS</span></span>

### <span data-ttu-id="c2060-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c2060-125">System.String</span></span>

## <span data-ttu-id="c2060-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2060-126">OUTPUTS</span></span>

### <span data-ttu-id="c2060-127">Microsoft. Azure. Command. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c2060-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>
<span data-ttu-id="c2060-128">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule, Microsoft. Azure. commands. DataLakeAnalytics, Version = 2.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c2060-128">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule, Microsoft.Azure.Commands.DataLakeAnalytics, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c2060-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2060-129">NOTES</span></span>

## <span data-ttu-id="c2060-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2060-130">RELATED LINKS</span></span>

