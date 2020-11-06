---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: cca9a398ad216de1bb28aac128fd9642b79d2dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493527"
---
# <span data-ttu-id="7d202-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7d202-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7d202-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d202-102">SYNOPSIS</span></span>
<span data-ttu-id="7d202-103">Tűzfal szabályait eltávolítja egy adattó-fiókból.</span><span class="sxs-lookup"><span data-stu-id="7d202-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d202-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d202-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d202-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d202-105">DESCRIPTION</span></span>
<span data-ttu-id="7d202-106">A **Remove-AzureRmDataLakeAnalyticsFirewallRule** parancsmag az Azure Data-tó Analytics-fiókjából távolítja el a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="7d202-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7d202-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7d202-107">EXAMPLES</span></span>

### <span data-ttu-id="7d202-108">1. példa: tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7d202-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="7d202-109">Ez a parancs eltávolítja a "saját tűzfalszabályok" nevű tűzfal-szabályt a "ContosoAdlAcct" fiókból.</span><span class="sxs-lookup"><span data-stu-id="7d202-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="7d202-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d202-110">PARAMETERS</span></span>

### <span data-ttu-id="7d202-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="7d202-111">-Account</span></span>
<span data-ttu-id="7d202-112">Az Data Lake Analytics-fiókja a tűzfalszabály eltávolításához</span><span class="sxs-lookup"><span data-stu-id="7d202-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="7d202-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d202-113">-Name</span></span>
<span data-ttu-id="7d202-114">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="7d202-114">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="7d202-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d202-115">-PassThru</span></span>
<span data-ttu-id="7d202-116">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7d202-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="7d202-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d202-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d202-118">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="7d202-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="7d202-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d202-119">-Confirm</span></span>
<span data-ttu-id="7d202-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d202-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d202-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d202-121">-WhatIf</span></span>
<span data-ttu-id="7d202-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d202-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d202-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d202-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d202-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d202-124">-DefaultProfile</span></span>
<span data-ttu-id="7d202-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d202-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d202-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d202-126">CommonParameters</span></span>
<span data-ttu-id="7d202-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d202-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d202-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d202-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d202-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d202-129">INPUTS</span></span>

### <span data-ttu-id="7d202-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7d202-130">System.String</span></span>
<span data-ttu-id="7d202-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7d202-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d202-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d202-132">OUTPUTS</span></span>

### <span data-ttu-id="7d202-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d202-133">System.Boolean</span></span>

## <span data-ttu-id="7d202-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d202-134">NOTES</span></span>

## <span data-ttu-id="7d202-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d202-135">RELATED LINKS</span></span>

