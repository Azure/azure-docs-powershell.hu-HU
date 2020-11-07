---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678935"
---
# <span data-ttu-id="4b06a-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b06a-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="4b06a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b06a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b06a-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="4b06a-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b06a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b06a-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b06a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b06a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b06a-106">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="4b06a-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="4b06a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4b06a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b06a-108">Törölje a AAD alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="4b06a-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="4b06a-109">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="4b06a-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="4b06a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b06a-110">PARAMETERS</span></span>

### <span data-ttu-id="4b06a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b06a-111">-DefaultProfile</span></span>
<span data-ttu-id="4b06a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b06a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b06a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4b06a-113">-Force</span></span>
<span data-ttu-id="4b06a-114">Ha megerősítés nélkül szeretne törölni egy alkalmazást, váltson.</span><span class="sxs-lookup"><span data-stu-id="4b06a-114">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b06a-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4b06a-115">-ObjectId</span></span>
<span data-ttu-id="4b06a-116">A törlendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4b06a-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b06a-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b06a-117">-Confirm</span></span>
<span data-ttu-id="4b06a-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b06a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b06a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b06a-119">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b06a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b06a-120">CommonParameters</span></span>
<span data-ttu-id="4b06a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b06a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b06a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b06a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b06a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b06a-123">INPUTS</span></span>

### <span data-ttu-id="4b06a-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="4b06a-124">None</span></span>
<span data-ttu-id="4b06a-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4b06a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b06a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b06a-126">OUTPUTS</span></span>

## <span data-ttu-id="4b06a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b06a-127">NOTES</span></span>
<span data-ttu-id="4b06a-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="4b06a-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4b06a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b06a-129">RELATED LINKS</span></span>

[<span data-ttu-id="4b06a-130">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b06a-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="4b06a-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b06a-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="4b06a-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b06a-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="4b06a-133">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4b06a-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

