---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297770"
---
# <span data-ttu-id="d05e0-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d05e0-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d05e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d05e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d05e0-103">A megadott megbízható identitás-szolgáltató eltávolítása a megadott Data Lake Store áruházból.</span><span class="sxs-lookup"><span data-stu-id="d05e0-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d05e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d05e0-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d05e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d05e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d05e0-106">A **Remove-AzDataLakeStoreTrustedIdProvider** parancsmag eltávolítja a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="d05e0-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d05e0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d05e0-107">EXAMPLES</span></span>

### <span data-ttu-id="d05e0-108">Példa 1: a megbízható identitás-szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d05e0-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="d05e0-109">A "MyProvider" szolgáltató eltávolítása a "ContosoADL" fiókból</span><span class="sxs-lookup"><span data-stu-id="d05e0-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="d05e0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d05e0-110">PARAMETERS</span></span>

### <span data-ttu-id="d05e0-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d05e0-111">-Account</span></span>
<span data-ttu-id="d05e0-112">Az Data Lake Store fiók a megbízható identitás-szolgáltató eltávolításához</span><span class="sxs-lookup"><span data-stu-id="d05e0-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="d05e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d05e0-113">-DefaultProfile</span></span>
<span data-ttu-id="d05e0-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d05e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d05e0-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d05e0-115">-Name</span></span>
<span data-ttu-id="d05e0-116">A megbízható identitás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="d05e0-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="d05e0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d05e0-117">-PassThru</span></span>
<span data-ttu-id="d05e0-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d05e0-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d05e0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d05e0-119">-ResourceGroupName</span></span>
<span data-ttu-id="d05e0-120">Annak a csoportnak a nevét adja meg, amely tartalmazza azt a fiókot, amelyből el szeretné távolítani a megbízható személyazonosság-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="d05e0-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="d05e0-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d05e0-121">-Confirm</span></span>
<span data-ttu-id="d05e0-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d05e0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d05e0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d05e0-123">-WhatIf</span></span>
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

### <span data-ttu-id="d05e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05e0-124">CommonParameters</span></span>
<span data-ttu-id="d05e0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d05e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05e0-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d05e0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05e0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d05e0-127">INPUTS</span></span>

### <span data-ttu-id="d05e0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d05e0-128">System.String</span></span>

### <span data-ttu-id="d05e0-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d05e0-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d05e0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d05e0-130">OUTPUTS</span></span>

### <span data-ttu-id="d05e0-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d05e0-131">System.Boolean</span></span>

## <span data-ttu-id="d05e0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d05e0-132">NOTES</span></span>

## <span data-ttu-id="d05e0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d05e0-133">RELATED LINKS</span></span>
