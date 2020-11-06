---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500719"
---
# <span data-ttu-id="24e8f-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="24e8f-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="24e8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="24e8f-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="24e8f-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24e8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24e8f-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e8f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="24e8f-106">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="24e8f-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="24e8f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24e8f-107">EXAMPLES</span></span>

### <span data-ttu-id="24e8f-108">--------------------------Törölje a AAD alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="24e8f-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="24e8f-109">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="24e8f-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="24e8f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24e8f-110">PARAMETERS</span></span>

### <span data-ttu-id="24e8f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="24e8f-111">-Force</span></span>
<span data-ttu-id="24e8f-112">Ha megerősítés nélkül szeretne törölni egy alkalmazást, váltson.</span><span class="sxs-lookup"><span data-stu-id="24e8f-112">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="24e8f-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="24e8f-113">-ObjectId</span></span>
<span data-ttu-id="24e8f-114">A törlendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="24e8f-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24e8f-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24e8f-115">-Confirm</span></span>
<span data-ttu-id="24e8f-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24e8f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e8f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e8f-117">-WhatIf</span></span>
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

### <span data-ttu-id="24e8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e8f-118">-DefaultProfile</span></span>
<span data-ttu-id="24e8f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24e8f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24e8f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e8f-120">CommonParameters</span></span>
<span data-ttu-id="24e8f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24e8f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e8f-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e8f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e8f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24e8f-123">INPUTS</span></span>

## <span data-ttu-id="24e8f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24e8f-124">OUTPUTS</span></span>

## <span data-ttu-id="24e8f-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24e8f-125">NOTES</span></span>
<span data-ttu-id="24e8f-126">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="24e8f-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="24e8f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24e8f-127">RELATED LINKS</span></span>

[<span data-ttu-id="24e8f-128">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="24e8f-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="24e8f-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="24e8f-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="24e8f-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="24e8f-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="24e8f-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="24e8f-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

