---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339558"
---
# <span data-ttu-id="f3afc-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3afc-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f3afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3afc-102">SYNOPSIS</span></span>
<span data-ttu-id="f3afc-103">Tűzfalszabály hozzáadása a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f3afc-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f3afc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3afc-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3afc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3afc-105">DESCRIPTION</span></span>
<span data-ttu-id="f3afc-106">Az **Add-AzDataLakeStoreFirewallRule parancsmag** hozzáad egy tűzfalszabályt a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f3afc-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f3afc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3afc-107">EXAMPLES</span></span>

### <span data-ttu-id="f3afc-108">1. példa: Új tűzfalszabály hozzáadása Data Lake Store-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="f3afc-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="f3afc-109">Ezzel létrehoz egy "MyRule" nevű új tűzfalszabályt a "ContosoADL" fiókban, 127.0.0.1-1-127.0.0.2 IP-tartománcával</span><span class="sxs-lookup"><span data-stu-id="f3afc-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="f3afc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3afc-110">PARAMETERS</span></span>

### <span data-ttu-id="f3afc-111">-Account</span><span class="sxs-lookup"><span data-stu-id="f3afc-111">-Account</span></span>
<span data-ttu-id="f3afc-112">The Data Lake Store account to add the firewall rule to</span><span class="sxs-lookup"><span data-stu-id="f3afc-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="f3afc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3afc-113">-DefaultProfile</span></span>
<span data-ttu-id="f3afc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f3afc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3afc-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3afc-115">-EndIpAddress</span></span>
<span data-ttu-id="f3afc-116">A tűzfalszabály érvényes IP-tartományának vége</span><span class="sxs-lookup"><span data-stu-id="f3afc-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3afc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f3afc-117">-Name</span></span>
<span data-ttu-id="f3afc-118">A hozzáadni megfelelő tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="f3afc-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="f3afc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3afc-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3afc-120">Annak az erőforráscsoportnak a neve, amely alatt a tűzfalszabály hozzáadásához szükséges fiók tartozik.</span><span class="sxs-lookup"><span data-stu-id="f3afc-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3afc-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3afc-121">-StartIpAddress</span></span>
<span data-ttu-id="f3afc-122">A tűzfalszabály érvényes IP-tartományának kezdete</span><span class="sxs-lookup"><span data-stu-id="f3afc-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3afc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3afc-123">-Confirm</span></span>
<span data-ttu-id="f3afc-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3afc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3afc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3afc-125">-WhatIf</span></span>
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

### <span data-ttu-id="f3afc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3afc-126">CommonParameters</span></span>
<span data-ttu-id="f3afc-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3afc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3afc-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3afc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3afc-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3afc-129">INPUTS</span></span>

### <span data-ttu-id="f3afc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f3afc-130">System.String</span></span>

## <span data-ttu-id="f3afc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3afc-131">OUTPUTS</span></span>

### <span data-ttu-id="f3afc-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3afc-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f3afc-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3afc-133">NOTES</span></span>

## <span data-ttu-id="f3afc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3afc-134">RELATED LINKS</span></span>
