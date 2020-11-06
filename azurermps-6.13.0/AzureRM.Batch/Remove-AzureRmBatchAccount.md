---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3528d66c635de78347647f0d1e451dc0b173a641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492866"
---
# <span data-ttu-id="ecf2d-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="ecf2d-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="ecf2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ecf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf2d-103">Egy köteg fiók eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecf2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ecf2d-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ecf2d-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf2d-106">A **Remove-AzureRmBatchAccount** parancsmag egy Azure-köteg-fiókot távolít el.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="ecf2d-107">Ez a parancsmag arra kéri, hogy mielőtt eltávolítja a fiókot, kivéve ha az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="ecf2d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ecf2d-108">EXAMPLES</span></span>

### <span data-ttu-id="ecf2d-109">1. példa: egy köteg fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ecf2d-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="ecf2d-110">Ez a parancs eltávolítja a pfuller nevű köteg-fiókot.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="ecf2d-111">Ez a parancs a fiók törlése előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="ecf2d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ecf2d-112">PARAMETERS</span></span>

### <span data-ttu-id="ecf2d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ecf2d-113">-AccountName</span></span>
<span data-ttu-id="ecf2d-114">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf2d-115">-DefaultProfile</span></span>
<span data-ttu-id="ecf2d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecf2d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ecf2d-117">-Force</span></span>
<span data-ttu-id="ecf2d-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf2d-119">-ResourceGroupName</span></span>
<span data-ttu-id="ecf2d-120">A parancsmag által eltávolított fiók erőforrás-csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ecf2d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ecf2d-121">-Confirm</span></span>
<span data-ttu-id="ecf2d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf2d-123">-WhatIf</span></span>
<span data-ttu-id="ecf2d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf2d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf2d-126">CommonParameters</span></span>
<span data-ttu-id="ecf2d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ecf2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf2d-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf2d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf2d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecf2d-129">INPUTS</span></span>

### <span data-ttu-id="ecf2d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf2d-130">System.String</span></span>

## <span data-ttu-id="ecf2d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecf2d-131">OUTPUTS</span></span>

### <span data-ttu-id="ecf2d-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="ecf2d-132">System.Void</span></span>

## <span data-ttu-id="ecf2d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ecf2d-133">NOTES</span></span>

## <span data-ttu-id="ecf2d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecf2d-134">RELATED LINKS</span></span>

[<span data-ttu-id="ecf2d-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="ecf2d-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="ecf2d-136">Új – AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="ecf2d-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="ecf2d-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="ecf2d-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="ecf2d-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ecf2d-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


