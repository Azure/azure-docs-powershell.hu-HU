---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679336"
---
# <span data-ttu-id="8bc95-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc95-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="8bc95-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bc95-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc95-103">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="8bc95-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bc95-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bc95-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc95-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bc95-105">DESCRIPTION</span></span>
<span data-ttu-id="8bc95-106">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="8bc95-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="8bc95-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8bc95-107">EXAMPLES</span></span>

### <span data-ttu-id="8bc95-108">--------------------------Törölje a AAD.</span><span class="sxs-lookup"><span data-stu-id="8bc95-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="8bc95-109">Törli a megadott Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="8bc95-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="8bc95-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bc95-110">PARAMETERS</span></span>

### <span data-ttu-id="8bc95-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8bc95-111">-Force</span></span>
<span data-ttu-id="8bc95-112">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="8bc95-112">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="8bc95-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8bc95-113">-ObjectId</span></span>
<span data-ttu-id="8bc95-114">A törlendő szolgáltató objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8bc95-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc95-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bc95-115">-PassThru</span></span>
<span data-ttu-id="8bc95-116">Ha meg van adva, akkor a törölt szolgáltatási megbízót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8bc95-116">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="8bc95-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8bc95-117">-Confirm</span></span>
<span data-ttu-id="8bc95-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8bc95-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc95-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc95-119">-WhatIf</span></span>
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

### <span data-ttu-id="8bc95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc95-120">-DefaultProfile</span></span>
<span data-ttu-id="8bc95-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bc95-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bc95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc95-122">CommonParameters</span></span>
<span data-ttu-id="8bc95-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bc95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc95-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc95-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc95-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bc95-125">INPUTS</span></span>

## <span data-ttu-id="8bc95-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bc95-126">OUTPUTS</span></span>

### <span data-ttu-id="8bc95-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc95-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="8bc95-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bc95-128">NOTES</span></span>
<span data-ttu-id="8bc95-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="8bc95-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8bc95-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bc95-130">RELATED LINKS</span></span>

[<span data-ttu-id="8bc95-131">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc95-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8bc95-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc95-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8bc95-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc95-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8bc95-134">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8bc95-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="8bc95-135">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8bc95-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
