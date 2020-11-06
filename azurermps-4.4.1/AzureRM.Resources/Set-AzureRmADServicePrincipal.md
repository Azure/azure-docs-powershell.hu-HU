---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 67af78e767b8da7764053e3652e25aef53f2877e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500700"
---
# <span data-ttu-id="859d0-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="859d0-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="859d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="859d0-102">SYNOPSIS</span></span>
<span data-ttu-id="859d0-103">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="859d0-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="859d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="859d0-104">SYNTAX</span></span>

### <span data-ttu-id="859d0-105">SpObjectIdWithDisplayNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="859d0-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="859d0-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="859d0-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859d0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="859d0-107">DESCRIPTION</span></span>
<span data-ttu-id="859d0-108">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="859d0-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="859d0-109">Ha frissíteni szeretné az ehhez a szolgáltatáshoz tartozó hitelesítő adatokat, használja az New-AzureRmADSpCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="859d0-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="859d0-110">Ha frissíteni szeretné a mögöttes alkalmazáshoz tartozó tulajdonságokat, használja az Set-AzureRmADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="859d0-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="859d0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="859d0-111">EXAMPLES</span></span>

### <span data-ttu-id="859d0-112">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="859d0-112">--------------------------  Example 1  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="859d0-113">Frissíti a szolgáltató megjelenítendő nevét a megadott objektumazonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="859d0-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="859d0-114">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="859d0-114">--------------------------  Example 2  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="859d0-115">Frissíti a szolgáltató megjelenítendő nevét a megadott egyszerű szolgáltatásnév használatával.</span><span class="sxs-lookup"><span data-stu-id="859d0-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="859d0-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="859d0-116">PARAMETERS</span></span>

### <span data-ttu-id="859d0-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="859d0-117">-DisplayName</span></span>
<span data-ttu-id="859d0-118">Az új megjelenítendő név a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="859d0-118">New display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="859d0-119">-ObjectId</span></span>
<span data-ttu-id="859d0-120">A frissítendő szolgáltatásnevet azonosító.</span><span class="sxs-lookup"><span data-stu-id="859d0-120">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-121">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="859d0-121">-ServicePrincipalName</span></span>
<span data-ttu-id="859d0-122">A frissítendő szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="859d0-122">The SPN of service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="859d0-123">-Confirm</span></span>
<span data-ttu-id="859d0-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="859d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859d0-125">-WhatIf</span></span>
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

### <span data-ttu-id="859d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859d0-126">-DefaultProfile</span></span>
<span data-ttu-id="859d0-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="859d0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="859d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859d0-128">CommonParameters</span></span>
<span data-ttu-id="859d0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="859d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859d0-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="859d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859d0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="859d0-131">INPUTS</span></span>

## <span data-ttu-id="859d0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="859d0-132">OUTPUTS</span></span>

## <span data-ttu-id="859d0-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="859d0-133">NOTES</span></span>

## <span data-ttu-id="859d0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="859d0-134">RELATED LINKS</span></span>

[<span data-ttu-id="859d0-135">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="859d0-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="859d0-136">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="859d0-136">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="859d0-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="859d0-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="859d0-138">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="859d0-138">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="859d0-139">Új – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="859d0-139">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="859d0-140">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="859d0-140">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

