---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 0f48bf7ad03dcfd59f8ea3653acdb7a57aa5240c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493688"
---
# <span data-ttu-id="7c791-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="7c791-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="7c791-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c791-102">SYNOPSIS</span></span>
<span data-ttu-id="7c791-103">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="7c791-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c791-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c791-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c791-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c791-105">DESCRIPTION</span></span>
<span data-ttu-id="7c791-106">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="7c791-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="7c791-107">Ha több olyan billentyű is létezik, amely ugyanazt a nevet adja, a lista első elemét eltávolítja a program.</span><span class="sxs-lookup"><span data-stu-id="7c791-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="7c791-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7c791-108">EXAMPLES</span></span>

### <span data-ttu-id="7c791-109">Példa 1 IotHub törlése</span><span class="sxs-lookup"><span data-stu-id="7c791-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="7c791-110">A "myiothub" nevű IotHub eltávolítja a iothubowner1 nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="7c791-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7c791-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c791-111">PARAMETERS</span></span>

### <span data-ttu-id="7c791-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c791-112">-DefaultProfile</span></span>
<span data-ttu-id="7c791-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7c791-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c791-114">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="7c791-114">-KeyName</span></span>
<span data-ttu-id="7c791-115">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="7c791-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c791-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c791-116">-Name</span></span>
<span data-ttu-id="7c791-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="7c791-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c791-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c791-118">-ResourceGroupName</span></span>
<span data-ttu-id="7c791-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="7c791-119">Resource Group Name</span></span>

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

### <span data-ttu-id="7c791-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c791-120">-Confirm</span></span>
<span data-ttu-id="7c791-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c791-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c791-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c791-122">-WhatIf</span></span>
<span data-ttu-id="7c791-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c791-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c791-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c791-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c791-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c791-125">CommonParameters</span></span>
<span data-ttu-id="7c791-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c791-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c791-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c791-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c791-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c791-128">INPUTS</span></span>

### <span data-ttu-id="7c791-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7c791-129">System.String</span></span>

## <span data-ttu-id="7c791-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c791-130">OUTPUTS</span></span>

### <span data-ttu-id="7c791-131">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7c791-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="7c791-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c791-132">NOTES</span></span>

## <span data-ttu-id="7c791-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c791-133">RELATED LINKS</span></span>
