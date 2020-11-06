---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: 9c512c1993700e1bbdab4d5c0d52a1aa2ceeafb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504259"
---
# <span data-ttu-id="97448-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97448-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="97448-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97448-102">SYNOPSIS</span></span>
<span data-ttu-id="97448-103">Eltávolít egy tárterület-fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="97448-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97448-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97448-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97448-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97448-105">DESCRIPTION</span></span>
<span data-ttu-id="97448-106">A **Remove-AzureRmStorageAccount** parancsmag eltávolítja a tárolási fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="97448-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="97448-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97448-107">EXAMPLES</span></span>

### <span data-ttu-id="97448-108">1. példa: tárterület-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="97448-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="97448-109">Ez a parancs eltávolítja a megadott tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="97448-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="97448-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97448-110">PARAMETERS</span></span>

### <span data-ttu-id="97448-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97448-111">-AsJob</span></span>
<span data-ttu-id="97448-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="97448-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97448-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97448-113">-DefaultProfile</span></span>
<span data-ttu-id="97448-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97448-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97448-115">-Force</span><span class="sxs-lookup"><span data-stu-id="97448-115">-Force</span></span>
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

### <span data-ttu-id="97448-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97448-116">-Name</span></span>
<span data-ttu-id="97448-117">Az eltávolítandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97448-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="97448-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97448-118">-ResourceGroupName</span></span>
<span data-ttu-id="97448-119">Az eltávolítandó tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97448-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="97448-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97448-120">-Confirm</span></span>
<span data-ttu-id="97448-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97448-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97448-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97448-122">-WhatIf</span></span>
<span data-ttu-id="97448-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97448-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97448-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97448-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97448-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97448-125">CommonParameters</span></span>
<span data-ttu-id="97448-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97448-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97448-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97448-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97448-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97448-128">INPUTS</span></span>

### <span data-ttu-id="97448-129">System. String</span><span class="sxs-lookup"><span data-stu-id="97448-129">System.String</span></span>

## <span data-ttu-id="97448-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97448-130">OUTPUTS</span></span>

### <span data-ttu-id="97448-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="97448-131">System.Void</span></span>

## <span data-ttu-id="97448-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97448-132">NOTES</span></span>

## <span data-ttu-id="97448-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97448-133">RELATED LINKS</span></span>

[<span data-ttu-id="97448-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97448-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="97448-135">Új – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97448-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="97448-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97448-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


