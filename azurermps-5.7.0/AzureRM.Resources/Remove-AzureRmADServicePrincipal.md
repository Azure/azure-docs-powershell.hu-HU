---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678932"
---
# <span data-ttu-id="18b84-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18b84-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="18b84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18b84-102">SYNOPSIS</span></span>
<span data-ttu-id="18b84-103">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="18b84-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18b84-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18b84-105">DESCRIPTION</span></span>
<span data-ttu-id="18b84-106">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="18b84-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="18b84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="18b84-107">EXAMPLES</span></span>

### <span data-ttu-id="18b84-108">Törölje a AAD-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="18b84-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="18b84-109">Törli a megadott Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="18b84-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="18b84-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18b84-110">PARAMETERS</span></span>

### <span data-ttu-id="18b84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b84-111">-DefaultProfile</span></span>
<span data-ttu-id="18b84-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="18b84-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18b84-113">-Force</span><span class="sxs-lookup"><span data-stu-id="18b84-113">-Force</span></span>
<span data-ttu-id="18b84-114">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="18b84-114">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="18b84-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="18b84-115">-ObjectId</span></span>
<span data-ttu-id="18b84-116">A törlendő szolgáltató objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="18b84-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b84-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18b84-117">-PassThru</span></span>
<span data-ttu-id="18b84-118">Ha meg van adva, akkor a törölt szolgáltatási megbízót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="18b84-118">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="18b84-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18b84-119">-Confirm</span></span>
<span data-ttu-id="18b84-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18b84-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b84-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b84-121">-WhatIf</span></span>
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

### <span data-ttu-id="18b84-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b84-122">CommonParameters</span></span>
<span data-ttu-id="18b84-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18b84-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b84-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b84-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b84-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18b84-125">INPUTS</span></span>

### <span data-ttu-id="18b84-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="18b84-126">None</span></span>
<span data-ttu-id="18b84-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="18b84-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18b84-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18b84-128">OUTPUTS</span></span>

### <span data-ttu-id="18b84-129">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18b84-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="18b84-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18b84-130">NOTES</span></span>
<span data-ttu-id="18b84-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="18b84-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="18b84-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18b84-132">RELATED LINKS</span></span>

[<span data-ttu-id="18b84-133">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18b84-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="18b84-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18b84-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="18b84-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="18b84-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="18b84-136">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="18b84-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="18b84-137">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="18b84-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
