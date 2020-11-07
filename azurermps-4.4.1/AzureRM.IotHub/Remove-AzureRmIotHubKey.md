---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 8b7603f145d45411b20b124823f28281d4117127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672220"
---
# <span data-ttu-id="36cae-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="36cae-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="36cae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36cae-102">SYNOPSIS</span></span>
<span data-ttu-id="36cae-103">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="36cae-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36cae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36cae-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36cae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36cae-105">DESCRIPTION</span></span>
<span data-ttu-id="36cae-106">Eltávolít egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="36cae-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="36cae-107">Ha több olyan billentyű is létezik, amely ugyanazt a nevet adja, a lista első elemét eltávolítja a program.</span><span class="sxs-lookup"><span data-stu-id="36cae-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="36cae-108">Példák</span><span class="sxs-lookup"><span data-stu-id="36cae-108">EXAMPLES</span></span>

### <span data-ttu-id="36cae-109">Példa 1 IotHub törlése</span><span class="sxs-lookup"><span data-stu-id="36cae-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="36cae-110">A "myiothub" nevű IotHub eltávolítja a iothubowner1 nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="36cae-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="36cae-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36cae-111">PARAMETERS</span></span>

### <span data-ttu-id="36cae-112">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="36cae-112">-KeyName</span></span>
<span data-ttu-id="36cae-113">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="36cae-113">Name of the Key</span></span>

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

### <span data-ttu-id="36cae-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36cae-114">-Name</span></span>
<span data-ttu-id="36cae-115">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="36cae-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="36cae-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36cae-116">-ResourceGroupName</span></span>
<span data-ttu-id="36cae-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="36cae-117">Resource Group Name</span></span>

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

### <span data-ttu-id="36cae-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36cae-118">-Confirm</span></span>
<span data-ttu-id="36cae-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36cae-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36cae-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36cae-120">-WhatIf</span></span>
<span data-ttu-id="36cae-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36cae-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36cae-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36cae-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36cae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cae-123">-DefaultProfile</span></span>
<span data-ttu-id="36cae-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36cae-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36cae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cae-125">CommonParameters</span></span>
<span data-ttu-id="36cae-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36cae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cae-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36cae-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cae-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36cae-128">INPUTS</span></span>

### <span data-ttu-id="36cae-129">System. String</span><span class="sxs-lookup"><span data-stu-id="36cae-129">System.String</span></span>

## <span data-ttu-id="36cae-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36cae-130">OUTPUTS</span></span>

### <span data-ttu-id="36cae-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="36cae-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="36cae-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36cae-132">NOTES</span></span>

## <span data-ttu-id="36cae-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36cae-133">RELATED LINKS</span></span>

