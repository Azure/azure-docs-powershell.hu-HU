---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 616502f91d93b39d1a778faea7b5e4de8b03dc23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666806"
---
# <span data-ttu-id="3ce97-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ce97-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3ce97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ce97-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce97-103">A megadott tűzfalszabályok módosítása a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="3ce97-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3ce97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ce97-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce97-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ce97-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce97-106">A **set-AzDataLakeStoreFirewallRule** parancsmag a megadott tűzfal-szabályt módosítja a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="3ce97-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3ce97-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ce97-107">EXAMPLES</span></span>

### <span data-ttu-id="3ce97-108">Példa 1: a tűzfalszabályok kezdési és befejezési IP-körének frissítése</span><span class="sxs-lookup"><span data-stu-id="3ce97-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="3ce97-109">A "ContosoADL" fiók "MyFirewallRule" ("") tűzfal-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="3ce97-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="3ce97-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ce97-110">PARAMETERS</span></span>

### <span data-ttu-id="3ce97-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="3ce97-111">-Account</span></span>
<span data-ttu-id="3ce97-112">Az Data Lake Store fiók a tűzfalszabályok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="3ce97-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="3ce97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce97-113">-DefaultProfile</span></span>
<span data-ttu-id="3ce97-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3ce97-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ce97-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ce97-115">-EndIpAddress</span></span>
<span data-ttu-id="3ce97-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="3ce97-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="3ce97-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ce97-117">-Name</span></span>
<span data-ttu-id="3ce97-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="3ce97-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="3ce97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce97-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ce97-120">Annak a csoportnak a nevét adja meg, amely a fiókot tartalmazza a tűzfalszabály frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="3ce97-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="3ce97-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ce97-121">-StartIpAddress</span></span>
<span data-ttu-id="3ce97-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="3ce97-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="3ce97-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ce97-123">-Confirm</span></span>
<span data-ttu-id="3ce97-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ce97-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce97-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce97-125">-WhatIf</span></span>
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

### <span data-ttu-id="3ce97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce97-126">CommonParameters</span></span>
<span data-ttu-id="3ce97-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ce97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce97-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce97-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce97-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ce97-129">INPUTS</span></span>

### <span data-ttu-id="3ce97-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3ce97-130">System.String</span></span>

## <span data-ttu-id="3ce97-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ce97-131">OUTPUTS</span></span>

### <span data-ttu-id="3ce97-132">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ce97-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3ce97-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ce97-133">NOTES</span></span>

## <span data-ttu-id="3ce97-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ce97-134">RELATED LINKS</span></span>
