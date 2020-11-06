---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3de75d2c8e7ed69a8f5be02833dd002ee5fbf016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500107"
---
# <span data-ttu-id="3d004-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3d004-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="3d004-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d004-102">SYNOPSIS</span></span>
<span data-ttu-id="3d004-103">Egy köteg fiók eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3d004-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d004-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d004-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d004-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d004-105">DESCRIPTION</span></span>
<span data-ttu-id="3d004-106">A **Remove-AzureRmBatchAccount** parancsmag egy Azure-köteg-fiókot távolít el.</span><span class="sxs-lookup"><span data-stu-id="3d004-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="3d004-107">Ez a parancsmag arra kéri, hogy mielőtt eltávolítja a fiókot, kivéve ha az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d004-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="3d004-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3d004-108">EXAMPLES</span></span>

### <span data-ttu-id="3d004-109">1. példa: egy köteg fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3d004-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="3d004-110">Ez a parancs eltávolítja a pfuller nevű köteg-fiókot.</span><span class="sxs-lookup"><span data-stu-id="3d004-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="3d004-111">Ez a parancs a fiók törlése előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d004-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="3d004-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d004-112">PARAMETERS</span></span>

### <span data-ttu-id="3d004-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d004-113">-AccountName</span></span>
<span data-ttu-id="3d004-114">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3d004-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3d004-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3d004-115">-Force</span></span>
<span data-ttu-id="3d004-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3d004-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d004-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d004-117">-ResourceGroupName</span></span>
<span data-ttu-id="3d004-118">A parancsmag által eltávolított fiók erőforrás-csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d004-118">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3d004-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d004-119">-Confirm</span></span>
<span data-ttu-id="3d004-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d004-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d004-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d004-121">-WhatIf</span></span>
<span data-ttu-id="3d004-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d004-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d004-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d004-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d004-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d004-124">-DefaultProfile</span></span>
<span data-ttu-id="3d004-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d004-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d004-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d004-126">CommonParameters</span></span>
<span data-ttu-id="3d004-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d004-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d004-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d004-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d004-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d004-129">INPUTS</span></span>

## <span data-ttu-id="3d004-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d004-130">OUTPUTS</span></span>

## <span data-ttu-id="3d004-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d004-131">NOTES</span></span>

## <span data-ttu-id="3d004-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d004-132">RELATED LINKS</span></span>

[<span data-ttu-id="3d004-133">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3d004-133">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="3d004-134">Új – AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3d004-134">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="3d004-135">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3d004-135">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="3d004-136">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3d004-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


