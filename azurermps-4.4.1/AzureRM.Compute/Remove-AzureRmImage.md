---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 7d6d130f639265cd2b7e2885f117d2e29899b8c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504192"
---
# <span data-ttu-id="feea1-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="feea1-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="feea1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="feea1-102">SYNOPSIS</span></span>
<span data-ttu-id="feea1-103">Eltávolít egy képet.</span><span class="sxs-lookup"><span data-stu-id="feea1-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feea1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="feea1-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feea1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="feea1-105">DESCRIPTION</span></span>
<span data-ttu-id="feea1-106">A **Remove-AzureRmImage** parancsmag eltávolítja a képet.</span><span class="sxs-lookup"><span data-stu-id="feea1-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="feea1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="feea1-107">EXAMPLES</span></span>

### <span data-ttu-id="feea1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="feea1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="feea1-109">Ez a parancs eltávolítja a "Image01" nevű képet a "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="feea1-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="feea1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="feea1-110">PARAMETERS</span></span>

### <span data-ttu-id="feea1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feea1-111">-DefaultProfile</span></span>
<span data-ttu-id="feea1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feea1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feea1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="feea1-113">-Force</span></span>
<span data-ttu-id="feea1-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="feea1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="feea1-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="feea1-115">-ImageName</span></span>
<span data-ttu-id="feea1-116">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="feea1-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feea1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feea1-117">-ResourceGroupName</span></span>
<span data-ttu-id="feea1-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="feea1-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="feea1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="feea1-119">-Confirm</span></span>
<span data-ttu-id="feea1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="feea1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feea1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feea1-121">-WhatIf</span></span>
<span data-ttu-id="feea1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="feea1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feea1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="feea1-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feea1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feea1-124">CommonParameters</span></span>
<span data-ttu-id="feea1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="feea1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feea1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feea1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feea1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="feea1-127">INPUTS</span></span>

### <span data-ttu-id="feea1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="feea1-128">System.String</span></span>

## <span data-ttu-id="feea1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feea1-129">OUTPUTS</span></span>

### <span data-ttu-id="feea1-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="feea1-130">System.Object</span></span>

## <span data-ttu-id="feea1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="feea1-131">NOTES</span></span>

## <span data-ttu-id="feea1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feea1-132">RELATED LINKS</span></span>

