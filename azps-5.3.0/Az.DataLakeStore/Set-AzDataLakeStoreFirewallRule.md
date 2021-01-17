---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465799"
---
# <span data-ttu-id="6cd22-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6cd22-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="6cd22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd22-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd22-103">Módosítja a megadott tűzfalszabályt a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="6cd22-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6cd22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cd22-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cd22-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cd22-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd22-106">A **Set-AzDataLakeStoreFirewallRule** parancsmag módosítja a megadott tűzfalszabályt a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="6cd22-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6cd22-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cd22-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd22-108">1. példa: Tűzfalszabály kezdő és záró IP-tartományának frissítése</span><span class="sxs-lookup"><span data-stu-id="6cd22-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="6cd22-109">A "ContosoADL" fiók "MyFirewallRule" tűzfalszabályának frissítése 127.0.0.1- 127.0.0.2 tartományra</span><span class="sxs-lookup"><span data-stu-id="6cd22-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="6cd22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cd22-110">PARAMETERS</span></span>

### <span data-ttu-id="6cd22-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6cd22-111">-Account</span></span>
<span data-ttu-id="6cd22-112">The Data Lake Store account to update the firewall rule in</span><span class="sxs-lookup"><span data-stu-id="6cd22-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="6cd22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd22-113">-DefaultProfile</span></span>
<span data-ttu-id="6cd22-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6cd22-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cd22-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="6cd22-115">-EndIpAddress</span></span>
<span data-ttu-id="6cd22-116">A tűzfalszabály érvényes IP-tartományának vége</span><span class="sxs-lookup"><span data-stu-id="6cd22-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="6cd22-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6cd22-117">-Name</span></span>
<span data-ttu-id="6cd22-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="6cd22-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="6cd22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd22-119">-ResourceGroupName</span></span>
<span data-ttu-id="6cd22-120">Annak az erőforráscsoportnak a neve, amely a tűzfalszabály frissítéséhez szükséges fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6cd22-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="6cd22-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="6cd22-121">-StartIpAddress</span></span>
<span data-ttu-id="6cd22-122">A tűzfalszabály érvényes IP-tartományának kezdete</span><span class="sxs-lookup"><span data-stu-id="6cd22-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="6cd22-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cd22-123">-Confirm</span></span>
<span data-ttu-id="6cd22-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cd22-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd22-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd22-125">-WhatIf</span></span>
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

### <span data-ttu-id="6cd22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd22-126">CommonParameters</span></span>
<span data-ttu-id="6cd22-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd22-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd22-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd22-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cd22-129">INPUTS</span></span>

### <span data-ttu-id="6cd22-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6cd22-130">System.String</span></span>

## <span data-ttu-id="6cd22-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cd22-131">OUTPUTS</span></span>

### <span data-ttu-id="6cd22-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6cd22-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="6cd22-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cd22-133">NOTES</span></span>

## <span data-ttu-id="6cd22-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cd22-134">RELATED LINKS</span></span>
