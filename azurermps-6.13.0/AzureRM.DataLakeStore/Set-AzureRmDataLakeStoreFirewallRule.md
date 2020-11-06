---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5b65e7f1dde9a4fc75e67b11cf4b7692a174add0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499555"
---
# <span data-ttu-id="405eb-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="405eb-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="405eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="405eb-102">SYNOPSIS</span></span>
<span data-ttu-id="405eb-103">A megadott tűzfalszabályok módosítása a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="405eb-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="405eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="405eb-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="405eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="405eb-105">DESCRIPTION</span></span>
<span data-ttu-id="405eb-106">A **set-AzureRmDataLakeStoreFirewallRule** parancsmag a megadott tűzfal-szabályt módosítja a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="405eb-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="405eb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="405eb-107">EXAMPLES</span></span>

### <span data-ttu-id="405eb-108">Példa 1: a tűzfalszabályok kezdési és befejezési IP-körének frissítése</span><span class="sxs-lookup"><span data-stu-id="405eb-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="405eb-109">A "ContosoADL" fiók "MyFirewallRule" ("") tűzfal-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="405eb-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="405eb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="405eb-110">PARAMETERS</span></span>

### <span data-ttu-id="405eb-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="405eb-111">-Account</span></span>
<span data-ttu-id="405eb-112">Az Data Lake Store fiók a tűzfalszabályok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="405eb-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="405eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405eb-113">-DefaultProfile</span></span>
<span data-ttu-id="405eb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="405eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="405eb-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="405eb-115">-EndIpAddress</span></span>
<span data-ttu-id="405eb-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="405eb-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405eb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="405eb-117">-Name</span></span>
<span data-ttu-id="405eb-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="405eb-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="405eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="405eb-120">Annak a csoportnak a nevét adja meg, amely a fiókot tartalmazza a tűzfalszabály frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="405eb-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="405eb-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="405eb-121">-StartIpAddress</span></span>
<span data-ttu-id="405eb-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="405eb-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="405eb-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="405eb-123">-Confirm</span></span>
<span data-ttu-id="405eb-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="405eb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="405eb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="405eb-125">-WhatIf</span></span>
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

### <span data-ttu-id="405eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405eb-126">CommonParameters</span></span>
<span data-ttu-id="405eb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="405eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405eb-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="405eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405eb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="405eb-129">INPUTS</span></span>

### <span data-ttu-id="405eb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="405eb-130">System.String</span></span>

## <span data-ttu-id="405eb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="405eb-131">OUTPUTS</span></span>

### <span data-ttu-id="405eb-132">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="405eb-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="405eb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="405eb-133">NOTES</span></span>

## <span data-ttu-id="405eb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="405eb-134">RELATED LINKS</span></span>
