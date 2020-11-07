---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: d3e7a04f292be8e83bc28456c0510450c078a777
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850526"
---
# <span data-ttu-id="f10be-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f10be-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="f10be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f10be-102">SYNOPSIS</span></span>
<span data-ttu-id="f10be-103">Eltávolít egy tárterület-fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="f10be-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f10be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f10be-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f10be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f10be-105">DESCRIPTION</span></span>
<span data-ttu-id="f10be-106">A **Remove-AzureRmStorageAccount** parancsmag eltávolítja a tárolási fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="f10be-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="f10be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f10be-107">EXAMPLES</span></span>

### <span data-ttu-id="f10be-108">1. példa: tárterület-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f10be-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="f10be-109">Ez a parancs eltávolítja a megadott tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="f10be-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="f10be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f10be-110">PARAMETERS</span></span>

### <span data-ttu-id="f10be-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f10be-111">-AsJob</span></span>
<span data-ttu-id="f10be-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f10be-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f10be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10be-113">-DefaultProfile</span></span>
<span data-ttu-id="f10be-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f10be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f10be-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f10be-115">-Force</span></span>
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

### <span data-ttu-id="f10be-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f10be-116">-Name</span></span>
<span data-ttu-id="f10be-117">Az eltávolítandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f10be-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="f10be-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f10be-118">-ResourceGroupName</span></span>
<span data-ttu-id="f10be-119">Az eltávolítandó tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f10be-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="f10be-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f10be-120">-Confirm</span></span>
<span data-ttu-id="f10be-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f10be-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f10be-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f10be-122">-WhatIf</span></span>
<span data-ttu-id="f10be-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f10be-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f10be-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f10be-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f10be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10be-125">CommonParameters</span></span>
<span data-ttu-id="f10be-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f10be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10be-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10be-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10be-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f10be-128">INPUTS</span></span>

### <span data-ttu-id="f10be-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f10be-129">System.String</span></span>

## <span data-ttu-id="f10be-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f10be-130">OUTPUTS</span></span>

### <span data-ttu-id="f10be-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="f10be-131">System.Void</span></span>

## <span data-ttu-id="f10be-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f10be-132">NOTES</span></span>

## <span data-ttu-id="f10be-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f10be-133">RELATED LINKS</span></span>

[<span data-ttu-id="f10be-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f10be-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="f10be-135">Új – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f10be-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="f10be-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f10be-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


