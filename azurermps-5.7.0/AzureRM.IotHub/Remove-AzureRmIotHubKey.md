---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 4f1c21f4f64193ec25a0392e094b8fd492ceba9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495344"
---
# <span data-ttu-id="4b1d0-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="4b1d0-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="4b1d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4b1d0-103">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4b1d0-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b1d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b1d0-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b1d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b1d0-105">DESCRIPTION</span></span>
<span data-ttu-id="4b1d0-106">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4b1d0-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="4b1d0-107">Ha több olyan billentyű is létezik, amely ugyanazt a nevet adja, a lista első elemét eltávolítja a program.</span><span class="sxs-lookup"><span data-stu-id="4b1d0-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="4b1d0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4b1d0-108">EXAMPLES</span></span>

### <span data-ttu-id="4b1d0-109">Példa 1 IotHub törlése</span><span class="sxs-lookup"><span data-stu-id="4b1d0-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="4b1d0-110">A "myiothub" nevű IotHub eltávolítja a iothubowner1 nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4b1d0-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4b1d0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b1d0-111">PARAMETERS</span></span>

### <span data-ttu-id="4b1d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1d0-112">-DefaultProfile</span></span>
<span data-ttu-id="4b1d0-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b1d0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b1d0-114">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="4b1d0-114">-KeyName</span></span>
<span data-ttu-id="4b1d0-115">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="4b1d0-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1d0-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b1d0-116">-Name</span></span>
<span data-ttu-id="4b1d0-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="4b1d0-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1d0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b1d0-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b1d0-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4b1d0-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1d0-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b1d0-120">-Confirm</span></span>
<span data-ttu-id="4b1d0-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b1d0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b1d0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b1d0-122">-WhatIf</span></span>
<span data-ttu-id="4b1d0-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4b1d0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b1d0-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b1d0-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b1d0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1d0-125">CommonParameters</span></span>
<span data-ttu-id="4b1d0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b1d0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1d0-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b1d0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1d0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b1d0-128">INPUTS</span></span>

### <span data-ttu-id="4b1d0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4b1d0-129">System.String</span></span>

## <span data-ttu-id="4b1d0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b1d0-130">OUTPUTS</span></span>

### <span data-ttu-id="4b1d0-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4b1d0-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4b1d0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b1d0-132">NOTES</span></span>

## <span data-ttu-id="4b1d0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b1d0-133">RELATED LINKS</span></span>

