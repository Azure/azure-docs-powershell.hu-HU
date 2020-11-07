---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 30a1599468851da5f01e10dc94af6586d3ecaf8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679090"
---
# <span data-ttu-id="d5ccf-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d5ccf-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="d5ccf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ccf-103">A megadott tűzfalszabályok módosítása a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="d5ccf-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5ccf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5ccf-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5ccf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ccf-106">A **set-AzureRmDataLakeStoreFirewallRule** parancsmag a megadott tűzfal-szabályt módosítja a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="d5ccf-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d5ccf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d5ccf-107">EXAMPLES</span></span>

### <span data-ttu-id="d5ccf-108">Példa 1: a tűzfalszabályok kezdési és befejezési IP-körének frissítése</span><span class="sxs-lookup"><span data-stu-id="d5ccf-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="d5ccf-109">A "ContosoADL" fiók "MyFirewallRule" ("") tűzfal-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="d5ccf-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="d5ccf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5ccf-110">PARAMETERS</span></span>

### <span data-ttu-id="d5ccf-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d5ccf-111">-Account</span></span>
<span data-ttu-id="d5ccf-112">Az Data Lake Store fiók a tűzfalszabályok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="d5ccf-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="d5ccf-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5ccf-113">-EndIpAddress</span></span>
<span data-ttu-id="d5ccf-114">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="d5ccf-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="d5ccf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5ccf-115">-Name</span></span>
<span data-ttu-id="d5ccf-116">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="d5ccf-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="d5ccf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ccf-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5ccf-118">Annak a csoportnak a nevét adja meg, amely a fiókot tartalmazza a tűzfalszabály frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d5ccf-118">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="d5ccf-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5ccf-119">-StartIpAddress</span></span>
<span data-ttu-id="d5ccf-120">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="d5ccf-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="d5ccf-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5ccf-121">-Confirm</span></span>
<span data-ttu-id="d5ccf-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5ccf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ccf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ccf-123">-WhatIf</span></span>
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

### <span data-ttu-id="d5ccf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ccf-124">-DefaultProfile</span></span>
<span data-ttu-id="d5ccf-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5ccf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5ccf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ccf-126">CommonParameters</span></span>
<span data-ttu-id="d5ccf-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5ccf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ccf-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ccf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ccf-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5ccf-129">INPUTS</span></span>

## <span data-ttu-id="d5ccf-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5ccf-130">OUTPUTS</span></span>

### <span data-ttu-id="d5ccf-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d5ccf-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="d5ccf-132">A frissített tűzfalszabály részletei.</span><span class="sxs-lookup"><span data-stu-id="d5ccf-132">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="d5ccf-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5ccf-133">NOTES</span></span>

## <span data-ttu-id="d5ccf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5ccf-134">RELATED LINKS</span></span>

