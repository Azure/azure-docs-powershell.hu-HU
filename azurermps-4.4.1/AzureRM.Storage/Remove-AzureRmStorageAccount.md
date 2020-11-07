---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: ba63794844420accf2e5e664a43f74b2578c780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672676"
---
# <span data-ttu-id="8139c-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8139c-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="8139c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8139c-102">SYNOPSIS</span></span>
<span data-ttu-id="8139c-103">Eltávolít egy tárterület-fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="8139c-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8139c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8139c-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8139c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8139c-105">DESCRIPTION</span></span>
<span data-ttu-id="8139c-106">A **Remove-AzureRmStorageAccount** parancsmag eltávolítja a tárolási fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="8139c-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="8139c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8139c-107">EXAMPLES</span></span>

### <span data-ttu-id="8139c-108">1. példa: tárterület-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8139c-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="8139c-109">Ez a parancs eltávolítja a megadott tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="8139c-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="8139c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8139c-110">PARAMETERS</span></span>

### <span data-ttu-id="8139c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8139c-111">-Force</span></span>
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

### <span data-ttu-id="8139c-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8139c-112">-Name</span></span>
<span data-ttu-id="8139c-113">Az eltávolítandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8139c-113">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="8139c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8139c-114">-ResourceGroupName</span></span>
<span data-ttu-id="8139c-115">Az eltávolítandó tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8139c-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="8139c-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8139c-116">-Confirm</span></span>
<span data-ttu-id="8139c-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8139c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8139c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8139c-118">-WhatIf</span></span>
<span data-ttu-id="8139c-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8139c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8139c-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8139c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8139c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8139c-121">-DefaultProfile</span></span>
<span data-ttu-id="8139c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8139c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8139c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8139c-123">CommonParameters</span></span>
<span data-ttu-id="8139c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8139c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8139c-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8139c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8139c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8139c-126">INPUTS</span></span>

## <span data-ttu-id="8139c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8139c-127">OUTPUTS</span></span>

## <span data-ttu-id="8139c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8139c-128">NOTES</span></span>

## <span data-ttu-id="8139c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8139c-129">RELATED LINKS</span></span>

[<span data-ttu-id="8139c-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8139c-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="8139c-131">Új – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8139c-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="8139c-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8139c-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


