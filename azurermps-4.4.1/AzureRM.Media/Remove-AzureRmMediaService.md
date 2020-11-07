---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9507cc178613a80ff0d49ed62e7e43698f5f1d7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679409"
---
# <span data-ttu-id="913fb-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="913fb-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="913fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="913fb-102">SYNOPSIS</span></span>
<span data-ttu-id="913fb-103">Adathordozó-szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="913fb-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="913fb-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="913fb-105">DESCRIPTION</span></span>
<span data-ttu-id="913fb-106">A **Remove-AzureRmMediaService** parancsmag eltávolítja a médiafájlt.</span><span class="sxs-lookup"><span data-stu-id="913fb-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="913fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="913fb-107">EXAMPLES</span></span>

### <span data-ttu-id="913fb-108">1. példa: a médiaadatfolyam-szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="913fb-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="913fb-109">Ez a parancs eltávolítja a MediaService0011 nevű médiafájlt a ResourceGroup001 nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="913fb-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="913fb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="913fb-110">PARAMETERS</span></span>

### <span data-ttu-id="913fb-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="913fb-111">-AccountName</span></span>
<span data-ttu-id="913fb-112">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="913fb-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913fb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="913fb-113">-Force</span></span>
<span data-ttu-id="913fb-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="913fb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="913fb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913fb-115">-ResourceGroupName</span></span>
<span data-ttu-id="913fb-116">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="913fb-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="913fb-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="913fb-117">-Confirm</span></span>
<span data-ttu-id="913fb-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="913fb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913fb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913fb-119">-WhatIf</span></span>
<span data-ttu-id="913fb-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="913fb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="913fb-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="913fb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913fb-122">-DefaultProfile</span></span>
<span data-ttu-id="913fb-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="913fb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="913fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913fb-124">CommonParameters</span></span>
<span data-ttu-id="913fb-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="913fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913fb-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913fb-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="913fb-127">INPUTS</span></span>

## <span data-ttu-id="913fb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="913fb-128">OUTPUTS</span></span>

### <span data-ttu-id="913fb-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="913fb-129">System.Boolean</span></span>

## <span data-ttu-id="913fb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="913fb-130">NOTES</span></span>

## <span data-ttu-id="913fb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="913fb-131">RELATED LINKS</span></span>

[<span data-ttu-id="913fb-132">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="913fb-132">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="913fb-133">Új – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="913fb-133">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="913fb-134">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="913fb-134">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


