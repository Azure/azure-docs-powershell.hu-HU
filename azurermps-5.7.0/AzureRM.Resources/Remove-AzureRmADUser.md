---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502479"
---
# <span data-ttu-id="87df4-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="87df4-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="87df4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87df4-102">SYNOPSIS</span></span>
<span data-ttu-id="87df4-103">Active Directory-felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="87df4-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87df4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87df4-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87df4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87df4-105">DESCRIPTION</span></span>
<span data-ttu-id="87df4-106">Egy Active Directory-felhasználó törlése (munkahelyi/iskolai fiók is ismert a szervezeti azonosító néven ismert).</span><span class="sxs-lookup"><span data-stu-id="87df4-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="87df4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87df4-107">EXAMPLES</span></span>

### <span data-ttu-id="87df4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="87df4-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="87df4-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="87df4-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="87df4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87df4-110">PARAMETERS</span></span>

### <span data-ttu-id="87df4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87df4-111">-DefaultProfile</span></span>
<span data-ttu-id="87df4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="87df4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87df4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="87df4-113">-Force</span></span>
<span data-ttu-id="87df4-114">Ha meg van adva, nem kér megerősítést a felhasználó törlésére.</span><span class="sxs-lookup"><span data-stu-id="87df4-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="87df4-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="87df4-115">-UPNOrObjectId</span></span>
<span data-ttu-id="87df4-116">A törölni kívánt felhasználó egyszerű felhasználónevét vagy objectId.</span><span class="sxs-lookup"><span data-stu-id="87df4-116">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87df4-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87df4-117">-Confirm</span></span>
<span data-ttu-id="87df4-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87df4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87df4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87df4-119">-WhatIf</span></span>
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

### <span data-ttu-id="87df4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87df4-120">CommonParameters</span></span>
<span data-ttu-id="87df4-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87df4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87df4-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87df4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87df4-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87df4-123">INPUTS</span></span>

### <span data-ttu-id="87df4-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="87df4-124">None</span></span>
<span data-ttu-id="87df4-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="87df4-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87df4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87df4-126">OUTPUTS</span></span>

## <span data-ttu-id="87df4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87df4-127">NOTES</span></span>

## <span data-ttu-id="87df4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87df4-128">RELATED LINKS</span></span>

[<span data-ttu-id="87df4-129">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="87df4-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="87df4-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="87df4-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="87df4-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="87df4-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

