---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: e92bdaae728031ba38fc1326ac2abb29aac86c59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195035"
---
# <span data-ttu-id="bb501-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb501-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="bb501-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb501-102">SYNOPSIS</span></span>
<span data-ttu-id="bb501-103">Eltávolít egy tárterület-fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="bb501-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="bb501-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb501-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb501-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb501-105">DESCRIPTION</span></span>
<span data-ttu-id="bb501-106">A **Remove-AzStorageAccount** parancsmag eltávolítja a tárolási fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="bb501-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="bb501-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bb501-107">EXAMPLES</span></span>

### <span data-ttu-id="bb501-108">1. példa: tárterület-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bb501-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="bb501-109">Ez a parancs eltávolítja a megadott tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="bb501-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="bb501-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb501-110">PARAMETERS</span></span>

### <span data-ttu-id="bb501-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb501-111">-AsJob</span></span>
<span data-ttu-id="bb501-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bb501-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb501-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb501-113">-DefaultProfile</span></span>
<span data-ttu-id="bb501-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb501-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb501-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bb501-115">-Force</span></span>
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

### <span data-ttu-id="bb501-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb501-116">-Name</span></span>
<span data-ttu-id="bb501-117">Az eltávolítandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb501-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb501-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb501-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb501-119">Az eltávolítandó tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb501-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb501-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb501-120">-Confirm</span></span>
<span data-ttu-id="bb501-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb501-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb501-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb501-122">-WhatIf</span></span>
<span data-ttu-id="bb501-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb501-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb501-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb501-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb501-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb501-125">CommonParameters</span></span>
<span data-ttu-id="bb501-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb501-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb501-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb501-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb501-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb501-128">INPUTS</span></span>

### <span data-ttu-id="bb501-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bb501-129">System.String</span></span>

## <span data-ttu-id="bb501-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb501-130">OUTPUTS</span></span>

### <span data-ttu-id="bb501-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="bb501-131">System.Void</span></span>

## <span data-ttu-id="bb501-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb501-132">NOTES</span></span>

## <span data-ttu-id="bb501-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb501-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb501-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb501-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="bb501-135">Új – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb501-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="bb501-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bb501-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

