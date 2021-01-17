---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465803"
---
# <span data-ttu-id="3076a-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3076a-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="3076a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3076a-102">SYNOPSIS</span></span>
<span data-ttu-id="3076a-103">A megadott megbízható identitásszolgáltató eltávolítása a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="3076a-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3076a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3076a-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3076a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3076a-105">DESCRIPTION</span></span>
<span data-ttu-id="3076a-106">A **Remove-AzDataLakeStoreTrustedIdProvider** parancsmag eltávolítja a megadott megbízható identitásszolgáltatót a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="3076a-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3076a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3076a-107">EXAMPLES</span></span>

### <span data-ttu-id="3076a-108">1. példa: Megbízható identitásszolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3076a-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="3076a-109">A "MyProvider" szolgáltató eltávolítása a "ContosoADL" fiókból</span><span class="sxs-lookup"><span data-stu-id="3076a-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="3076a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3076a-110">PARAMETERS</span></span>

### <span data-ttu-id="3076a-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3076a-111">-Account</span></span>
<span data-ttu-id="3076a-112">The Data Lake Store account to remove the trusted identity provider from</span><span class="sxs-lookup"><span data-stu-id="3076a-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="3076a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3076a-113">-DefaultProfile</span></span>
<span data-ttu-id="3076a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3076a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3076a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3076a-115">-Name</span></span>
<span data-ttu-id="3076a-116">A megbízható identitásszolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="3076a-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="3076a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3076a-117">-PassThru</span></span>
<span data-ttu-id="3076a-118">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="3076a-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="3076a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3076a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3076a-120">Annak az erőforráscsoportnak a nevét adja meg, amely azt a fiókot tartalmazza, amelyből el szeretné távolítani a megbízható identitásszolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="3076a-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="3076a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3076a-121">-Confirm</span></span>
<span data-ttu-id="3076a-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3076a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3076a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3076a-123">-WhatIf</span></span>
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

### <span data-ttu-id="3076a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3076a-124">CommonParameters</span></span>
<span data-ttu-id="3076a-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3076a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3076a-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3076a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3076a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3076a-127">INPUTS</span></span>

### <span data-ttu-id="3076a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3076a-128">System.String</span></span>

### <span data-ttu-id="3076a-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3076a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3076a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3076a-130">OUTPUTS</span></span>

### <span data-ttu-id="3076a-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3076a-131">System.Boolean</span></span>

## <span data-ttu-id="3076a-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3076a-132">NOTES</span></span>

## <span data-ttu-id="3076a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3076a-133">RELATED LINKS</span></span>
