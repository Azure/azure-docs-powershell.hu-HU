---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: bed4ec4fd3afdf0218f68d9e2e4c61c739db48ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498983"
---
# <span data-ttu-id="f30d0-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f30d0-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f30d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f30d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f30d0-103">Tűzfal-szabályt ad hozzá az adattó-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f30d0-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f30d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f30d0-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f30d0-105">DESCRIPTION</span></span>
<span data-ttu-id="f30d0-106">Az **Add-AzureRmDataLakeAnalyticsFirewallRule** parancsmag tűzfal-szabályt ad az Azure Data Lake-tó Analytics-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="f30d0-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f30d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f30d0-107">EXAMPLES</span></span>

### <span data-ttu-id="f30d0-108">1. példa: tűzfalszabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f30d0-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="f30d0-109">Ez a parancs hozzáadja a "My Firewall Rule" nevű tűzfal-szabályt a "ContosoAdlAcct" fiókból az IP-tartománnyal: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="f30d0-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="f30d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f30d0-110">PARAMETERS</span></span>

### <span data-ttu-id="f30d0-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="f30d0-111">-Account</span></span>
<span data-ttu-id="f30d0-112">Az Data Lake Analytics-fiók a tűzfalszabály hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="f30d0-112">The Data Lake Analytics account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30d0-113">-DefaultProfile</span></span>
<span data-ttu-id="f30d0-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f30d0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f30d0-115">-EndIpAddress</span></span>
<span data-ttu-id="f30d0-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="f30d0-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f30d0-117">-Name</span></span>
<span data-ttu-id="f30d0-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="f30d0-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="f30d0-120">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="f30d0-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f30d0-121">-StartIpAddress</span></span>
<span data-ttu-id="f30d0-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="f30d0-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f30d0-123">-Confirm</span></span>
<span data-ttu-id="f30d0-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f30d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30d0-125">-WhatIf</span></span>
<span data-ttu-id="f30d0-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f30d0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30d0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f30d0-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30d0-128">CommonParameters</span></span>
<span data-ttu-id="f30d0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f30d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30d0-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30d0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30d0-131">INPUTS</span></span>

### <span data-ttu-id="f30d0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f30d0-132">System.String</span></span>

## <span data-ttu-id="f30d0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30d0-133">OUTPUTS</span></span>

### <span data-ttu-id="f30d0-134">Microsoft. Azure. Command. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f30d0-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f30d0-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f30d0-135">NOTES</span></span>

## <span data-ttu-id="f30d0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f30d0-136">RELATED LINKS</span></span>

