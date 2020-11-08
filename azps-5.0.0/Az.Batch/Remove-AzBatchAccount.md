---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187080"
---
# <span data-ttu-id="2c8f7-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2c8f7-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="2c8f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8f7-103">Egy köteg fiók eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-103">Removes a Batch account.</span></span>

## <span data-ttu-id="2c8f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c8f7-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c8f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c8f7-105">DESCRIPTION</span></span>
<span data-ttu-id="2c8f7-106">A **Remove-AzBatchAccount** parancsmag egy Azure-köteg-fiókot távolít el.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="2c8f7-107">Ez a parancsmag arra kéri, hogy mielőtt eltávolítja a fiókot, kivéve ha az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="2c8f7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2c8f7-108">EXAMPLES</span></span>

### <span data-ttu-id="2c8f7-109">1. példa: egy köteg fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2c8f7-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="2c8f7-110">Ez a parancs eltávolítja a pfuller nevű köteg-fiókot.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="2c8f7-111">Ez a parancs a fiók törlése előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="2c8f7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c8f7-112">PARAMETERS</span></span>

### <span data-ttu-id="2c8f7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c8f7-113">-AccountName</span></span>
<span data-ttu-id="2c8f7-114">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c8f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8f7-115">-DefaultProfile</span></span>
<span data-ttu-id="2c8f7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c8f7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2c8f7-117">-Force</span></span>
<span data-ttu-id="2c8f7-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c8f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c8f7-120">A parancsmag által eltávolított fiók erőforrás-csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c8f7-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c8f7-121">-Confirm</span></span>
<span data-ttu-id="2c8f7-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c8f7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c8f7-123">-WhatIf</span></span>
<span data-ttu-id="2c8f7-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c8f7-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c8f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8f7-126">CommonParameters</span></span>
<span data-ttu-id="2c8f7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c8f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8f7-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c8f7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8f7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c8f7-129">INPUTS</span></span>

### <span data-ttu-id="2c8f7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2c8f7-130">System.String</span></span>

## <span data-ttu-id="2c8f7-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c8f7-131">OUTPUTS</span></span>

### <span data-ttu-id="2c8f7-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="2c8f7-132">System.Void</span></span>

## <span data-ttu-id="2c8f7-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c8f7-133">NOTES</span></span>

## <span data-ttu-id="2c8f7-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c8f7-134">RELATED LINKS</span></span>

[<span data-ttu-id="2c8f7-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2c8f7-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="2c8f7-136">Új – AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2c8f7-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="2c8f7-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2c8f7-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="2c8f7-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2c8f7-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
